# Mòdul Odoo: Assegurances (examen SGE 2026)

![CFGS DAM](https://img.shields.io/badge/CFGS-Desenvolupament%20d%27Aplicacions%20Multiplataforma%20%28DAM%29-green?style=for-the-badge)
![SGE](https://img.shields.io/badge/assignatura-Sistemes%20de%20Gesti%C3%B3%20Empresarial-purple?style=for-the-badge)
![Odoo](https://img.shields.io/badge/Odoo-18-714B67?style=for-the-badge&logo=odoo&logoColor=white)

Mòdul d'Odoo per gestionar pòlisses d'assegurança. Va ser l'examen de l'assignatura de Sistemes de Gestió Empresarial (SGE) del CFGS de Desenvolupament d'Aplicacions Multiplataforma (Institut Milà i Fontanals, Igualada) del 2026.

## Models

- **`insurance.policy`**: pòlissa amb prenedor (client), producte assegurat, corredor (proveïdor), objecte assegurat, dates d'efecte, anul·lació i venciment, hora d'efecte, motiu d'anul·lació i tipus de venciment (anual, semestral, trimestral o mensual). La data de venciment es calcula a partir de la data d'efecte i el tipus.
- **`insurance.reason`**: motius d'anul·lació de pòlisses.
- **`res.partner`** (ampliat): mostra les pòlisses d'un contacte, tant com a prenedor com a corredor.

## Regles de negoci

- La data d'anul·lació no pot ser anterior a la data d'efecte.
- La data d'efecte no pot ser en el passat.
- El prenedor ha de ser client (`customer_rank > 0`) i el corredor, proveïdor (`supplier_rank > 0`).

## Altres elements

- Vistes, accions i menús per a pòlisses i motius.
- Informe PDF de pòlissa (`report/report.xml`).
- Seguretat i dades de demostració.

## Instal·lació

1. Copia la carpeta al directori `addons` d'Odoo i reinicia el servidor.
2. Actualitza la llista d'aplicacions i instal·la **insurance_pratssara**.
3. Dependències: `base`, `product`, `sale` i `purchase`.

## Autoria

Sara Prats Morales · Llicència LGPL-3

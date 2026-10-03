# UCS-Library — Archived

> **ARCHIVED (read-only).** Union Catalog Server - katalog union antar perpustakaan (lineage SLiMS/Simbio2). Snapshot terakhir: **Februari 2023**.

> **Catatan:** ini kode **legacy tanpa wrapper modern** (PHP prosedural + `dbc.inc.php`, tanpa composer, tanpa test, tanpa CI). Kalau ada instance UCS yang masih hidup, repo ini tidak dihapus - hanya beku.

## Kenapa di-archive

- Tidak ada commit sejak 2023, nol issue, nol test.
- Endpoints OAI/record (`oai2.php`, `record_dc.php`, `ucpoll.php`) berasal dari era 2010-an, dan tidak ada yang mengembangkannya lagi.
- Penting: **`Unida-Library` tidak bergantung pada repo ini.** Sistemnya berdiri sendiri, jadi meng-archive repo tidak mematikan instance mana pun yang sedang jalan.

## Kalau butuh sesuatu

| Butuh | Untuk |
|---|---|
| Sinkronisasi katalog antar kampus | `UCS-Library` (`ucpoll.php`, OAI-PMH) - read-only, fork dulu |
| Katalog lokal single-site | `Unida-Library` -> `app/Livewire/Opac/` |
| Sinkronisasi Repository ke Unida | `Unida-Library` -> `routes/api_v1.php` (mobile API) dan `repo-unida` (EPrints/OAI) |

## Peringatan

Jangan menulis ke `includes/`, `admin/`, `themes/` di sini tanpa owner instance yang jelas - repo sudah tidak bisa di-commit.
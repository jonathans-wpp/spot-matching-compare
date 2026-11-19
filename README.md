# Spot Matching Compare

Halaman untuk membandingkan Drop File sistem (SpotPlan + SpotMatch dari Spot Matching) dengan Drop File September.

Buka: https://jonathans-wpp.github.io/spot-matching-compare/

## Cara pakai

1. Drop file .xlsx sistem di kotak **Sistem** dan file September di kotak **September** (boleh banyak file).
2. Klik **Bandingkan**. File dipasangkan lewat nomor BB (10 digit) di nama file atau nama sheet, lalu dibandingkan per sheet tanpa peduli urutan baris dan kolom.
3. Klik baris BB untuk melihat detail, atau **Download CSV beda**.

Kolom identitas dan kolom yang diabaikan bisa diubah di panel **Cara mencocokkan baris**.

Kolom biaya SpotPlan (`Net_Cost`, `CPRP_Cost`, `GroupCPRP`, `Gross_Cost`, `Cash_Discount`) dibanding sampai 2 desimal. Selisih di bawah itu (noise angka Excel) tidak dihitung beda, hanya ditandai kuning sebagai catatan.

## Data

File hanya dibaca di browser dan tidak dikirim ke mana pun. File, pengaturan, dan status banding disimpan di browser (IndexedDB dan localStorage), jadi tetap ada setelah refresh. Tombol **×** menghapus satu file, **Reset** menghapus semuanya.

Satu-satunya dependency adalah [SheetJS](https://sheetjs.com/) dari cdnjs.

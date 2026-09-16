NEOSHY WEB — Rombak Account Center
==================================

Perubahan utama:
1. Semua pengelolaan data web hanya lewat 1 halaman: manage/account.html
   - Manage Service  → tombol portal ke manage/index.html
   - Manage Vault (link download) → tombol portal ke vault/admin.html
   - Manage Akun: username login, password, email baru, upload + crop foto profil

2. Halaman utama (index.html & main/index.html):
   - Kanan atas: tombol "Login"
   - Setelah login: tampil username + foto profil (dari localStorage neoshy_profile)
   - Klik → masuk Account Center
   - Portal "Service Manager" di halaman publik DIHAPUS

3. Vault (vault/index.html):
   - Tombol admin lama diganti → "Account Center" (hanya muncul jika sudah login)
   - Tidak ada manage file langsung di halaman vault publik

4. Setelah login sukses → redirect ke manage/account.html

Cara replace:
- Backup project lama
- Copy semua isi folder "NEOSHY WEB FULL" ke project kamu
- Pastikan file logo.png, wa-qr.png, dan folder tools/assets tetap ada
- Supabase URL & key sudah sama seperti sebelumnya

Struktur:
  index.html          → landing utama (Account-centric)
  main/index.html     → versi alternatif (path relatif ../)
  manage/account.html → CONTROL CENTER (semua manage di sini)
  manage/index.html   → Service Manager
  manage/dashboard.html
  vault/index.html    → Vault download publik
  vault/admin.html    → Vault Manager (akses dari Account)
  tools/              → Remote tools page


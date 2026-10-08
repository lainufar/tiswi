# GLOSARIUM

Kumpulan istilah dan singkatan yang dipakai di repo ini.

| Istilah | Kepanjangan / Arti |
|---|---|
| **M3U / M3U8** | MP3 URL / MP3 URL versi UTF-8 — berkas teks daftar alamat siaran (playlist) yang dibaca pemutar video. |
| **IPTV** | *Internet Protocol Television* — siaran TV yang dikirim lewat jaringan internet, bukan antena/kabel. |
| **OTT** | *Over-The-Top* — layanan TV/video yang berjalan di atas internet, tanpa operator TV kabel (contoh aplikasi: VLC, TiviMate, OTT Navigator, IPTV Smarters). |
| **Stream** | Aliran data video/audio yang dikirim terus-menerus (bukan berkas yang diunduh utuh). |
| **HLS** | *HTTP Live Streaming* — protokol streaming berbasis HTTP; berkasnya berakhiran `.m3u8`. |
| **m3u8** | Format playlist HLS (lihat M3U). |
| **ffprobe** | Alat dari paket **FFmpeg** untuk memeriksa isi stream: apakah ada video & audio, resolusinya berapa. |
| **ffmpeg** | Perangkat lunak sumber terbuka untuk mengolah video/audio; di sini dipakai menguji apakah stream benar-benar bisa didekode. |
| **UA / User-Agent** | *User-Agent* — identitas "aplikasi pengakses" yang dikirim ke server; sebagian server menolak selain UA tertentu. |
| **Referer** | Alamat halaman asal yang dikirim ke server; sebagian penyiar mensyaratkan ini agar stream tidak ditolak (403). |
| **403 Forbidden** | Kode balasan server: permintaan ditolak (mis. karena UA/Referer/geolokasi tidak sesuai). |
| **404 Not Found** | Kode balasan server: alamat stream tidak ditemukan / sudah mati. |
| **Geo-blocked** | Dibatasi hanya bisa diakses dari wilayah/negara tertentu. |
| **[Not 24/7]** | Channel tidak mengudara sepanjang 24 jam (kadang kosong pada jam-jam tertentu). |
| **RAW** | Tampilan berkas apa adanya di GitHub (tanpa antarmuka web), dipakai untuk menyalin URL playlist. |
| **tvg-id** | *TV Guide ID* — pengenal channel untuk sinkronisasi panduan acara (EPG). |
| **tvg-name** | Nama channel sesuai katalog EPG. |
| **EPG** | *Electronic Program Guide* — panduan acara TV elektronik (jadwal siaran). |
| **group-title** | Label kelompok/grup channel di dalam playlist (mis. "Indonesia", "Discovery"). |
| **EXTVLCOPT** | Baris opsi khusus VLC (mis. menyetel Referer/User-Agent) di dalam berkala M3U. |
| **Repo** | *Repository* — tempat penyimpanan berkas & riwayat perubahan, umumnya di GitHub. |
| **Commit** | Satu rekaman perubahan berkas di dalam repo git. |
| **Push** | Mengirim commit dari komputer lokal ke repo di GitHub. |
| **GitHub Actions** | Layanan otomatisasi GitHub; di repo ini dipakai menjalankan verifikasi berkala. |

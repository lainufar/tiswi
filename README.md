# IPTV Indonesia Terverifikasi 🇮🇩

Playlist **M3U** channel televisi Indonesia + **Discovery Channel**, **Red Bull TV** (olahraga),
dan channel **Petualangan/Alam** — setiap tautan sudah **diuji benar-benar bisa diputar**
(bukan sekadar daftar mentah).

> Terakhir diverifikasi: **8 Oktober 2026** · Cara uji: unduh 5 detik video nyata via `ffmpeg`
> (`-t 5 -f null`) setelah lolos `ffprobe`; hanya yang **benar-benar mendekode audio/video** yang masuk daftar.

## Isi repo

| Berkas | Keterangan | Jumlah |
|---|---|---|
| `playlists/iptv-indonesia-all.m3u` | Semua channel (4 kategori) | **174** |
| `playlists/indonesia.m3u` | TV nasional & daerah Indonesia | **98** |
| `playlists/discovery.m3u` | Discovery Channel & saudaranya | **5** |
| `playlists/redbull.m3u` | Red Bull TV (olahraga ekstrem) | **2** |
| `playlists/petualangan.m3u` | Petualangan, alam, satwa, traveling | **69** |
| `data/channels.csv` | Daftar channel + URL (untuk Excel/Sheets) | 174 |
| `data/channels.json` | Daftar channel (untuk aplikasi/API) | 174 |
| `tools/verify_playlist.py` | Skrip verifikasi ulang mandiri | — |

## Cara pakai

**1. Aplikasi OTT / pemutar di TV & HP** (VLC, TiviMate, OTT Navigator, IPTV Smarters,
Kodi, PotPlayer, MX Player, Smart TV):

- Unduh berkas `.m3u` di atas (tombol **Raw** → simpan), lalu buka sebagai playlist.
- Atau salurkan langsung lewat URL **Raw**, contoh:
  `https://raw.githubusercontent.com/<USER>/<REPO>/main/playlists/iptv-indonesia-all.m3u`

**2. VLC di komputer:** Media → Open Network Stream → tempel URL Raw di atas.

> Sebagian channel butuh **Referer** atau **User-Agent** khusus. Berkas `.m3u` ini sudah
> menyertakan baris `#EXTVLCOPT` untuk itu (dipakai VLC/Kodi); pemutar lain biasanya
> mengabaikannya dan tetap jalan untuk mayoritas channel.

## Cara verifikasi ulang sendiri

```bash
pip install -r tools/requirements.txt   # lalu pastikan ffmpeg & ffprobe terpasang
python tools/verify_playlist.py playlists/iptv-indonesia-all.m3u
```

Skrip mengecek tiap stream: `ffprobe` (ada audio+video?) lalu `ffmpeg` (mampu dekode 5 detik?).
Hanya yang lolos dua tahap dicatat sebagai valid.

## Catatan keandalan

- Channel IPTV publik **sifatnya berubah-ubah**. Sebagian bertanda `[Not 24/7]` (tidak mengudara
  24 jam) dan `[Geo-blocked]` (perlu lokasi tertentu).
- Playlist **bukan sumber resmi penyiar**; semua tautan diambil dari katalog publik
  [iptv-org](https://github.com/iptv-org/iptv). Hak siar tetap milik masing-masing penyiar.
- Daftar ini **bebas kredensial** — tidak memuat token/akun apa pun.

## Lisensi

Skrip & berkas pendukung: [MIT](LICENSE). Daftar tautan disediakan apa adanya ("as is"),
tanpa jaminan ketersediaan.

## Istilah

Lihat **GLOSARIUM.md** untuk arti M3U, ffprobe, OTT, RAW, dan singkatan lain.

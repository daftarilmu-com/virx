# Welcome to DDX-ID by DAFTARILMU.COM

Sebuah repository serverless tunnel studi kasus Indonesia

> ## NOTES.md
>
> Kamu tidak perlu membayar untuk menggunakan kode dalam repository/layanan ini.  
> Kalau kamu membayar kepada siapapun, berarti kamu terkena scam.

# Fitur

- [x] Otomatis split protocol VLESS, Trojan, dan Shadowsocks
- [x] Reverse proxy
- [x] Cache daftar proxy
- [x] Support TCP dan DoH
- [x] Transport Websocket CDN dan SNI
- [x] KV proxy key (proxy berdasarkan country)
- [x] Pagination
- [x] Tampilan web bagus dan minimalis (Menurut saya)
- [x] Dark mode
- [x] Auto check (ping) akun
- [x] Ambil akun dalam beberapa format (link, clash, sing-box, dll)
- [x] Registrasi wildcard
- [x] Menambahkan filter
  - [x] Negara `&cc=ID,SG,...`
- [x] Subscription API
  - [x] Country Code `&cc=ID,SG,JP,KR,...`
  - [x] Format `&format=clash` (raw, clash, sfa, bfr, v2ray)
  - [x] Limit `&limit=10`
  - [x] VPN `&vpn=vless,trojan,ss`
  - [x] Port `&port=443,80`
  - [x] Domain `&domain=zoom.us`
- [x] Tombol `Deploy to workers` untuk instant deployment

# Todo (Belum Selesai)

- [x] Lebih efisien (Partial) (I hate Javascript btw, jadi males buat benerin)
- [ ] Skema URL shadowsocks

Kode ini masih perlu banyak perbaikan, jadi silahkan berkontribusi dan berikan PR kalian!

# Catatan

- Harus UUID v4 Variant 2
- Gunakan security `none`
- Gunakan DoH di aplikasi VPN kalian jika tidak bisa browsing atau membuka website
  - Contoh DoH `https://8.8.8.8/dns-query`

# Cara Deploy

## Manual

1. Buat akun cloudflare
2. Buat worker pilih [hello world] deploy
3. Klik EDITOR
4. Copy kode dari `_worker.js` ke editor cloudflare worker
5. GANTI SEMUA DENGAN PUNYA MU:
6. const rootDomain = "dediwebsx.workers.dev"; 
const serviceName = "pro"; 
const apiKey = "DOJac7cindcoo_xB1N5Q9tjB3NSbyWlHEPAiKOr"; 
const apiEmail = "dediwebx@gmail.com"; 
const accountID = "b4fcd4d07f838466cbbc9d9502604a"; 
const zoneID = "083ac8642a453e8fe1c02347a065fc"; 
7. (Optional) Masukkan link daftar proxy kalian ke dalam environemnt variable `PROXY_BANK_URL`
8. (Optional) Masukkan link target reverse proxy ke environment variable `REVERSE_PROXY_TARGET`
9. Deploy
10. Buka `https://DOMAIN_WORKER_KALIAN/sub`




## Cara Aktivasi API

Berikut cara aktivasinya:
1. Buka dan login cloudflare
2. Buka Manage Account dan pilih Account API tokens
3. Create Token
4. pilih use template > Edit Cloudflare Workers
5. Zone Resources kemudian pilih > include > all zone > pilih email mu
6. Continue summary
7. Done, copy Api Token 






# DEMO

[Demo Cloudflare Workers](https://demo.kurniaonelove.workers.dev/)

# Footnote


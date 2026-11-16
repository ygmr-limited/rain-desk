# HukukDesk

HukukDesk, YGMR Danışmanlık Ltd. Şti.'nin uzak masaüstü / uzaktan destek ürünüdür.
[RustDesk](https://github.com/rustdesk/rustdesk) 1.5.3 (AGPL-3.0) tabanlıdır; değiştirilmiş kaynak AGPL-3.0 kapsamında sunulur.

## Değişiklikler (RustDesk 1.5.3'e göre)
- Uygulama adı `HukukDesk`, ORG `com.ygmr` (`libs/hbb_common/src/config.rs`)
- Varsayılan bağlantı sunucusu `38.210.77.209` + sunucu açık anahtarı
- Windows dosya bilgileri (`Cargo.toml`)
- `hbb_common` alt modülü depoya gömüldü (tek depo)
- CI yalnız Windows x64 (`.github/workflows/hukukdesk.yml` → elle başlatılır)
- Ad değiştiği için RustDesk güncelleme kontrolü kendiliğinden kapalı (`is_custom_client`)

## Sunucu
`38.210.77.209:/srv/hukukdesk` — Docker `hukukdesk-hbbs` + `hukukdesk-hbbr` (rustdesk-server 1.1.14, `-k _` anahtar zorunlu).
Portlar: 21115–21117/tcp, 21116/udp.

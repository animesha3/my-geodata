# my-geodata

[![Update geosite](https://github.com/animesha3/my-geodata/actions/workflows/update-geosite.yml/badge.svg)](https://github.com/animesha3/my-geodata/actions/workflows/update-geosite.yml)

Автоматическая сборка `geosite.dat` для Xray/V2Ray.

## Скачать

- [geosite.dat](https://raw.githubusercontent.com/animesha3/my-geodata/main/release/geosite.dat)
- [SHA-256](https://raw.githubusercontent.com/animesha3/my-geodata/main/release/geosite.dat.sha256)

Ссылки становятся доступны после первой успешной сборки.

## Источники

- Все категории [hydraponique/roscomvpn-geosite](https://github.com/hydraponique/roscomvpn-geosite/tree/master/data).
- [category-ip-geo-detect](https://github.com/v2fly/domain-list-community/blob/master/data/category-ip-geo-detect) из v2fly/domain-list-community и зависимости include.
- Компилятор: [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community).

Категории сохраняются отдельно. Например: `geosite:category-ip-geo-detect`, `geosite:youtube`, `geosite:whitelist`. Наличие категории не назначает ей direct/proxy/block: это задаётся в конфигурации маршрутизации. Это выборочная база, а не полная замена всех категорий стандартного geosite.dat.

## Обновления

GitHub Actions проверяет источники каждый день в 03:23 UTC (05:23 Калининград). При изменениях исходные списки, лицензии и собранная база коммитятся в main. Запуск вручную: Actions → Update geosite → Run workflow. Запуск по расписанию может задерживаться; GitHub отключает расписание в публичном репозитории после 60 дней без активности.

`data/` генерируется автоматически: изменения вручную будут перезаписаны. `licenses/` содержит лицензии исходных проектов. Изменения README не запускают сборку.

## GeoIP

`geoip.dat` не входит в эту сборку: указанные источники содержат домены. Для него нужен отдельный источник IP/CIDR.

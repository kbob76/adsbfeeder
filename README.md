# ADS-B Feeder
ADS-B Feeder Project

Leverages SDR-Enthusiasts Ultrafeeder docker image to feed ADS-B flight data to various flight data exchanges (FlightAware, FlightRadar24, etc). 

## Active Feeds
| Site          | Feeding Data? |
| ------------- | ------------- | 
| FlightAware   | Yes           |
| FlightRadar24 | Yes           |
| ADSB Exchange | Yes           |

## Docker Images
Ultrafeeder - https://github.com/sdr-enthusiasts/docker-adsb-ultrafeeder?tab=readme-ov-file#mlat-configuration

PiAware - https://github.com/sdr-enthusiasts/docker-piaware

FlightRadar24 - https://github.com/sdr-enthusiasts/docker-flightradar24

## Metrics Monitoring

NOTE: Ultrafeeder image does not come with telegraf, must use the `telegraf` image tag to get the docker image with telegraf installed.

Metrics sent to Prometheus and InfluxDB, Grafana for visualization and monitoring

## Future Work
- Pull ACARS data down
- Setup granular alerting for various planes 

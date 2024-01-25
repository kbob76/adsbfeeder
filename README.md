# adsbfeeder
ADS-B Feeder Project

Leverages SDR-Enthusiasts Ultrafeeder docker image to feed ADS-B flight data to various flight data exchanges (FlightAware, FlightRadar24, etc). Currently under development

### DEV Issues
When deploying Prometheus you need to exec into the docker image and update the Prometheus.yml file, see the command below

```
docker exec -it prometheus sh -c "echo -e \" - job_name: 'ultrafeeder'\n static_configs:\n - targets: ['ultrafeeder:9273']\" >> /etc/prometheus/prometheus.yml"
```

All this does is just add in the following to the YAML file: 
```
- job_name: 'ultrafeeder'
  static_configs:
  - targets: ['ultrafeeder:9273']
```


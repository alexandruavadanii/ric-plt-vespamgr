# RIC VESPA manager

The VESPA manager uses the VES Agent (https://github.com/nokia/ONAP-VESPA)
to adapt near-RT RIC internal statistics' collection using Prometheus 
(xApps and platform containers) to ONAP's VES (VNF event streaming).

The VESPA manager starts and configures the VES Agent.

# Environment variables

The VESPA manager container requires the following environment variables:

* VESMGR_HB_INTERVAL - VES heartbeat interval. For example: 30s.
* VESMGR_MEAS_INTERVAL - Measurement interval. For example: 60s.
* VESMGR_PRICOLLECTOR_ADDR - Primary collector IP address. For example: 127.0.0.1.
* VESMGR_PRICOLLECTOR_PORT - Primary collector port id as an integer. For example: 1234.
* VESMGR_PROMETHEUS_ADDR - Prometheus address. For example: http://127.0.0.1:123

# Unit Tests

In order to run the VESPA manager unit tests, give the following command:

```
go test ./... -v
```

# License

See [LICENSES.txt](LICENSES.txt) file.
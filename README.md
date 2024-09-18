# P99 Conf - Elevating PostgreSQL: Benchmarking Vector Search Performance  - Data Set

This repo contains the associated raw benchmark results of the [P99 Conf talk  Elevating PostgreSQL: Benchmarking Vector Search Performance](https://www.p99conf.io/). 

The `results` folder contains the data for the four discussed benchmark cases:
- `pgvector` index types
- `pgvector` index creation time
- `pgvecto.rs` performance
- `pgvector` vs. `pgvecto.rs` 

For more details on the method and the benchmark objectives please refer to conference talk.

Each folder contains the data of a single run benchmark of one configuration. 

***

## Data Set Structure


In order to ensure full transparency and reproducibility,  each data folder contains benchmark configuration data,  performance data, monitoring data, cloud provider metadata, VM metadata and DBMS configuration data.
 

***

### Benchmark Configuration Data

All configurable benchmark parameters for PostgreSQL and VectorDBBench are defined in the `evaluationScenario.json`.

The `benchANT_versions` contains the used versions of the benchANT software components to execute the benchmarks. 

The execution logs of the individual benchmark steps are contained in `airflowTaskInstanceDetails.json`. 

***

### Performance Data

The raw performance data output of the VectorDBBench is contained in the `0_load.txt`  for the LOAD, OPTIMIZE and QUERY phase. 

***

### Monitoring Data

The DBMS cluster and the benchmark instances are monitored with [Telegraf](https://github.com/influxdata/telegraf) and the data is stored in [InfluxDB](https://github.com/influxdata/influxdb). 

A full snapshot of the monitoring data of each run is contained in the  `influx_data.zip` file.


*** 

### Cloud Provider Metadata

The cloud provider metadata for the DBMS deployment is contained in the `dbms_data_resources.json` / `dbms_management_resources.json` and for the benchmark deployment in the `benchmark_resources.json`. 


*** 

### VM Metadata

The VM metadata for the DBMS deployment is contained in the `dbms_data_hardware_facts.json` / `dbms_management_hardware_facts.json` and for the benchmark deployment in the `benchmark_hardware_facts.json`.  


*** 

### DBMS Metadata

For each DBMS, relevant configuration files and cluster states are stored before executing the workload. 

DBMS-specific files are contained in each folder, e.g. `postgresql.conf` for PostgreSQL DBMS deployments. 

*** 


## Contact

In case of questions or feedback on the data feel free to create an issue or reach out to info@benchant.com


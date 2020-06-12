# ODBC for Hive

Tested on HDP 2.6.5

## Usage

Set-up your `.odbc.ini` and mount it in root home folder(`/root`)

Example with current path :

```bash
docker run --rm -it --mount type=bind,source="$(pwd)",target=/root hiveodbc:v1
```

You can use the sql client provided with unixodbc

`isql WebDB MyID MyPWD -w < My.sql`

how to pass secret (login/password) => use env file : https://docs.docker.com/compose/environment-variables/#the-env-file

## HDP

The Hortonworks Hive ODBC Driver files are installed in the following directories: `/usr/lib/hive/lib/native/hiveodbc/`

The Hortonworks Hive ODBC Driver files are installed in the following directories:

- /usr/lib/hive/lib/native/hiveodbc/ErrorMessages – Error messages files directory
- /usr/lib/hive/lib/native/hiveodbc/Setup – Sample configuration files directory
- /usr/lib/hive/lib/native/Linux-i386-32 – 32-bit shared libraries directory
- /usr/lib/hive/lib/native/Linux-amd64-64 – 64-bit shared libraries directory

The configuration files are:

- `.odbc.ini` The file used to define ODBC data sources (required)
- `.odbcinst.ini` The file used to define ODBC drivers (optional)
- `.hortonworks.hiveodbc.ini` – The file used to configure the Hortonworks Hive ODBC Driver (required)

## HDP Requirements

- Red Hat® Enterprise Linux® (RHEL) 5.0, CentOS 5.0 or SUSE Linux Enterprise Server (SLES)
- Both 32 and 64-bit editions are supported.
- An installed ODBC Driver Manager, for example (iODBC 3.52.7 or above or unixODBC 2.3.0 or above)

## Notes

Official open source project hive does not support ODBC

> There is no ODBC driver available for HiveServer2 as part of Apache Hive. There are third party ODBC drivers available from different vendors, and most of them seem to be free.

[ref](https://cwiki.apache.org/confluence/display/Hive/HiveODBC)

## References

- [unixodbc](http://www.unixodbc.org/odbcinst.html)
- [HDP ODBC/JDBC](https://docs.cloudera.com/HDPDocuments/HDP2/HDP-2.6.5/bk_data-access/content/hive-jdbc-odbc-drivers.html)
- [Horton system requirements](https://hortonworks.com/wp-content/uploads/2013/04/Hortonworks-Hive-ODBC-Driver-User-Guide.pdf)

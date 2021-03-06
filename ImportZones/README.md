# Import Zones

This is a console example of importing zones from a .csv file.

Steps:

1. Process command line arguments: Server, Database, Username, Password, Input File and load .csv file.
1. Create Geotab API object and Authenticate.
1. Import zones into database.

> the .csv file included in this project is a sample, you may need to change entries (such as group names) for the example to work.

## Prerequisites

The sample application requires:

- [.Net core 2.0 SDK](https://dot.net/core) or higher

## CSV layout

name | longitude | latitude | size | group name

```csv
# importZones.csv
# Structure: <name>, <longitude>, <latitude>, <size>, <groupName>
# -------------------------------------------------------------------------
# lines beginning with '#' are comments and ignored
Customer 1,40.68775,-73.98997,200,Company Group
```

## Getting started

```shell
> git clone https://github.com/Geotab/sdk-dotnet-samples.git sdk-dotnet-samples
> cd sdk-dotnet-samples
> cd ImportZones
> dotnet run "my.geotab.com" "database" "user@email.com" "password" "--poly=4" "--type=customer" "importZones.csv"
```

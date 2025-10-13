The two key metrics which can tell you if your server is lagging are the **ticks per second** (`TPS`) and the **milliseconds per tick** (`MSPT`).

## What is a good TPS?

In general, you want to keep your TPS at `20.00` at all times. If your server drops below `19 TPS` frequently, it is worth investigating the source of lag using [Spark](https://spark.lucko.me).

## What is a good MSPT?

You should always aim for an MSPT below `40`. That will allow for random ticks which may take longer than average, without facing any lag issues.

If your MSPT goes above `50`, the server will start to lag and you should investigate the source of the lag using [Spark](https://spark.lucko.me/).

## Checking the TPS

On Bukkit-based server softwares, you can run the `/tps` command to check the ticks per second of your server.

This should give a result like this if your server is not lagging:

```
TPS from last 1m, 5m, 15m: 20.0, 20.0, 19.9
```

If it instead outputs something like this, you should look into ways to optimise your server or find the source of the lag:

```
TPS from last 1m, 5m, 15m: 12.1, 8.4, 9.7
```

## Checking the MSPT

### Bukkit-based servers (e.g. Paper)

On Bukkit-based server, you can check the MSPT using the `/mspt` command. It should output something as follows:

```
Server tick times (avg/min/max) from last 5s, 10s, 1m:
◴ 30.0/24.8/40.4, 31.1/24.8/51.7, 27.2/15.1/57.7
```

The first number in each 'group' is the **average** MSPT and is the most important. If that goes above ~40, you should look into optimising the server.

If you have a maximum MSPT of over 80 (the last number of each 'group' of numbers), you should look into [finding lag spikes using Spark](https://spark.lucko.me/docs/guides/Finding-lag-spikes).

### Vanilla or Fabric servers

Check the MSPT using the `/tick query` command. This will output something like the following:

```
The game is running normally
Target tick rate: 20.0 per second.
Average time per tick: 36.3ms (Target: 50.0ms)
Percentiles: P50: 35.6ms P95: 46.0ms P99: 47.8ms, sample: 100
```

If your average time per tick is over `40.0ms`, you should look into optimisation.

Similarly, if your `P99` percentile (similar to the `max` above) is over 80, you should look into [finding the cause of the lag spikes](https://spark.lucko.me/docs/guides/Finding-lag-spikes).

## The `/tpsbar` command on Purpur

If you run a Purpur server, you can monitor the TPS, MSPT and your ping live using the `/tpsbar` command.

This will show a bossbar at the top of your screen showing the server tick rates, and will go red if the TPS goes below 20.

## My server is lagging - how do I fix it?

See if you can find the cause using Spark first. If not, send a spark report in our Discord server and we'll be happy to help!

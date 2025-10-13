
Setting a worldborder is useful if you don't want your players building too far away from spawn, or if you want to keep your storage usage low.

## How to set the size of the world border

```
/worldborder set <diameter>
```

For example, to set a worldborder of diameter `1000`, you would run:

```
/worldborder set 1000
```

> Note that a diameter of 1000, for example, means that the world will have a *radius* of `500`. This means that (if the world border was centered at `0,0`), the world would stretch from `-250` to `250`, **not** `500`.

## Configuring the center of the worldborder

To set the center of the world border, run this command, replacing `[x]` and `[y]` with the `x` and `y` coordinates of your world center:

```
/worldborder center [x] [y]
```

If you are standing at the `x` and `y` position you want to make the world center, you can simply run:

```
/worldborder center
```

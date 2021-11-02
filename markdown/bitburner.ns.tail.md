<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [NS](./bitburner.ns.md) &gt; [tail](./bitburner.ns.tail.md)

## NS.tail() method

Opens a script’s logs. This is functionally the same as the tail Terminal command.

If the function is called with no arguments, it will open the current script’s logs.

Otherwise, the fn, hostname/ip, and args… arguments can be used to get the logs from another script. Remember that scripts are uniquely identified by both their names and arguments.

<b>Signature:</b>

```typescript
tail(fn?: string, host?: string, ...args: any[]): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  fn | string | Optional. Filename of the script being tailed. If omitted, the current script is tailed. |
|  host | string | Optional. Hostname of the script being tailed. Defaults to the server this script is running on. If args are specified, this is not optional. |
|  args | any\[\] | Arguments for the script being tailed. |

<b>Returns:</b>

void

## Remarks

RAM cost: 0 GB

## Example 1


```ts
//Open logs from foo.script on the current server that was run with no args
tail("foo.script");
```

## Example 2


```ts
//Get logs from foo.script on the foodnstuff server that was run with no args
tail("foo.script", "foodnstuff");
```

## Example 3


```ts
//Get logs from foo.script on the foodnstuff server that was run with the arguments [1, "test"]
tail("foo.script", "foodnstuff", 1, "test");
```

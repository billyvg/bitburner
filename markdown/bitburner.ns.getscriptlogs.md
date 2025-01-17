<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [NS](./bitburner.ns.md) &gt; [getScriptLogs](./bitburner.ns.getscriptlogs.md)

## NS.getScriptLogs() method

Get all the logs of a script.

<b>Signature:</b>

```typescript
getScriptLogs(fn?: string, host?: string, ...args: any[]): string[];
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  fn | string | Optional. Filename of script to get logs from. |
|  host | string | Optional. Hostname of the server that the script is on. |
|  args | any\[\] | Arguments to identify which scripts to get logs for. |

<b>Returns:</b>

string\[\]

Returns an string array, where each line is an element in the array. The most recently logged line is at the end of the array.

## Remarks

RAM cost: 0 GB

Returns a script’s logs. The logs are returned as an array, where each line is an element in the array. The most recently logged line is at the end of the array. Note that there is a maximum number of lines that a script stores in its logs. This is configurable in the game’s options. If the function is called with no arguments, it will return the current script’s logs.

Otherwise, the fn, hostname/ip, and args… arguments can be used to get the logs from another script. Remember that scripts are uniquely identified by both their names and arguments.

## Example 1


```ts
//Get logs from foo.script on the current server that was run with no args
getScriptLogs("foo.script");
```

## Example 2


```ts
//Open logs from foo.script on the foodnstuff server that was run with no args
getScriptLogs("foo.script", "foodnstuff");
```

## Example 3


```ts
//Open logs from foo.script on the foodnstuff server that was run with the arguments [1, "test"]
getScriptLogs("foo.script", "foodnstuff", 1, "test");
```


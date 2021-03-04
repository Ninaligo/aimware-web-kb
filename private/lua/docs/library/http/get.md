# http.Get
Get data from a URL.

## Syntax
```
http.Get(url:string, callback:optional)
```

## Parameters
```url``` URL to fetch.

```callback``` _optional_ Callback function.

## Return value

```data``` Returns web page body at given URL.

!!! note
	To make this call non-blocking specify **callback(body)** function as second
	argument.

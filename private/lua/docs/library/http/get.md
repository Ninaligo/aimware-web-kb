# http.Get
Returns web page body at given URL.

## Syntax
```
http.Get(url:string, callback:optional)
```

## Parameters
```url``` URL to fetch.

```callback``` _optional_ Callback function.

## Return value
This function has no return value.

!!! note
	To make this call non-blocking specify **callback(body)** function as second
	argument.

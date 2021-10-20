## Insight Config Set-Target

Set the metadata store endpoint.

### Synopsis

Set the target endpoint for the metadata store.

```
insight config set-target <endpoint> [--ca-cert <ca certificate path to verify peer against>] [--access-token <kubernetes service account access token>] [flags]
```

### Examples

```
insight config set-target https://localhost:8443 --ca-cert=/tmp/ca.crt --access-token eyJhbGc...
```

### Options

```
      --access-token string   Kubernetes access token. It is recommended to use the Environment Variable METADATA_STORE_ACCESS_TOKEN during the API calls, this will override access token flag. Note: using the the access-token flag stores the token on disk, the Environment Variable is retrieved at the time of the API call
      --ca-cert string        trusted ca certificate
  -h, --help                  help for set-target
```

### SEE ALSO

* [insight config](insight_config.md)	 - Config commands

###### Auto generated by spf13/cobra on 27-Sep-2021
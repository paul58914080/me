## Install

Install **Java** using [SDKMAN](../sdkman/index.md) with the following command:

```shell
sdk install java 21.0.2-tem
```

## Configuration

### Certificates

To list the certificates in the keystore, use the following command:

```shell
keytool -list -keystore [keystore] -storepass [storepass]
```

To add a certificate to the keystore, use the following command:

```shell
keytool -import -alias [alias] -keystore [keystore] \ 
        -storepass [storepass] -file [certificate]
```


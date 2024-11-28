## web

1.Generate a seed and return its hexadecimal string.

```
seed = api.export_new_seed();
```

2.Pass in the seed, and return the private key handle.

```
privatePkey = api.import_prikey_handler_from_seed(seed);
```

3.Pass in the private key handle, and it will return the hexadecimal encoding of the private key.

```
hexprikey = api.export_new_prikey_to_hex(privatePkey);
```

4.Pass in the hexadecimal encoding of the private key and return the private key handle

```
api.import_prikey_handler_from_hex(hexprikey);
```

5.Pass in the private key handle and return the addr account address of the private key

```
addr = api.get_addr(privatePkey);
resultaddr = api.get_addr(hexresultHandler);
console.assert(addr == resultaddr, "fail to recover private key");
```

6.Release the private key handle

```
api.free_prikey_handler(hexresultHandler);
```

7.Pass in the hexadecimal seed and return the seed mnemonic 

```
mnemonic = api.export_mnemonic_from_seed(seed);
```

8.Pass in seed mnemonics, return hexadecimal seeds

```
mnemonicresultHandler = api.import_seed_from_mnemonic(mnemonic);
```

9.Pass in the private key handle and return the base64 encoding of the public key

```
base64pubkey = api.get_pubstr_base64(privatePkey);
```

10.Get the transaction body. Here, use the GetTransaction rpc interface to get the ordinary transaction body (see rpc documentation for details).

```json
//req
{
    "id": "",
    "jsonrpc": "",
    "params": {
        "fromAddr": [
            "cED97dA085527Fe7e1772CA59Aa1e64A78143128"
        ],
        "isFindUtxo": false,
        "toAddr": [
            {
                "addr": "06BA76F46631d4F344d1344303895001F1E3Af29",
                "value": "13.5"
            }
        ],
        "txInfo": ""
    }
}
//ack
{
  "id": "",
  "jsonrpc": "",
  "method": "GetTransaction",
  "result": {
    "code": 0,
    "gas": "20200",
    "height": "2506",
    "message": "success",
    "time": "1717557136905780",
    "txJson": "{\"time\":\"1717557136905780\",\"identity\":\"0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"26cc05fef65e94c15d759a27a24a57793253f25a3dece8e7761024ab0d0220dd\"}]}],\"vout\":[{\"value\":\"1350000000\",\"addr\":\"06BA76F46631d4F344d1344303895001F1E3Af29\"},{\"value\":\"1978395583553\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"20200\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":1}",
    "txType": "0",
    "vrfJson": "{}"
  }
}
```
There are two ways to sign transactions. The first way is to take out the transaction field txjson for signature and backfill the signature result, which does not distinguish the transaction type and is easy to maintain later; the second way is to directly sign according to the transaction type, which is convenient to use, and only needs to judge the transaction type before use, which is not easy to maintain later

11.Sign the non-" contract "transaction returned by GetTransaction, pass in the message to be signed, the message length, and the private key handle, and return the signed message

```
message = tx;
message_size = message.length;
signature = api.sig_tx(message,message_size,privatePkey);
```

12Sign the "contract" transaction returned by GetTransaction, pass in the message to be signed, the message length, and the private key handle, and return the signed transaction json
```
message = tx;
message_size = message.length;
signature = api.sig_contract_tx(message,message_size,privatePkey);
```

13.Sign "txJson" in the "result" field of the transaction return value, pass in the message to be signed and the private key handle, and return the signed message

```
txJson = ...;
message = txJson;
message_size = message.length;
signature = api.txJsonSign(message,privatePkey);
```

14.Sign the transaction returned by GetTransaction, pass in the message to be signed, the message length and the private key handle, and return the signed message

```
message = tx;
message_size = message.length;
signature = api.sig_tx(message,message_size,privatePkey);
```
15.Put the signed information back into the txJson of the transaction body, and send the transaction to the node through the SendMessage rpc interface to complete the sending transaction (see rpc document for details).

```json
//Data after signing the data returned by GetTransaction
{
    "id": "",
    "jsonrpc": "",
    "result": {
        "code": "",
        "gas": "20200",
        "height": "600",
        "message": "",
        "time": "1717148047269517",
        "txJson": "{\"time\":\"1717148047269517\",\"identity\":\"2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"3f1342e96e426e2905021ad991787131ec70d31298646b1e80da9d912eeff274\"}],\"vinSign\":{\"sign\":\"ApxL8NDgh9YYDuUXpdbsbVv0cEAr3HyXmr2TICkD4mfuDIZqVlZJNUmaPAKHCs5kkn7JnZx7r12+CpnnR4ZpAg==\",\"pub\":\"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=\"}}],\"vout\":[{\"value\":\"1350000000\",\"addr\":\"06BA76F46631d4F344d1344303895001F1E3Af29\"},{\"value\":\"1982446992477\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"20200\",\"addr\":\"VirtualBurnGas\"}],\"multiSign\":[{\"sign\":\"WCoFsLKML69x1rSpQc7pwbnd+GMfZ0Ce3wTPg96Rdb1v7ezFw9KuEBXwvGecTz264pVZB6T8hzgJIx26GuKVAA==\",\"pub\":\"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":1}",
        "txType": "1",
        "vrfJson": "{\"vrfdata\":{\"hash\":\"6cf89d80c98eecd9138caca4f55d7ad0fda2aed9d8e68dd4642543ae3ee056d6\"},\"Vrfsign\":{\"sign\":\"u5dNZ16Rd77B4nLd8gAcKTwz+GxeHH1HIlcGennGbPaKgIFXUkmFzS/EnVxRC4nmSfESAdWyMEmj4pKBhwuqAg==\",\"pub\":\"MCowBQYDK2VwAyEAcUcydwF7CSr9bjBiUbd3drV+WMd4yd8xFL7HWGA4FTw=\"}}"
    }
}
```

16.After the public key, message, and signed message are passed in, the verification result of the signed message is returned. 0 indicates success and -1 indicates failure

```
result = api.verif_by_public_str(base64pubkey, base64pubkey.length, message, message_size, signature, signature.length);
```

17.Other interfaces return the sdk version

```
version = api.get_version()
```

## Mobile terminal

### IOS

**Note: Except for the get_version interface, other interfaces with a return value of char* use free to free the heap space occupied by the return value**

```c
/**
* @brief       Return the sdk version number
* @return      const char* : Version information
*/
const char *get_version();

/**
* @brief       Pass in the base64 encoding of the private key and return the private key handle
* @param       buf: base64 encoding of the private key
* @param       buf_size: base64 encoding length of the private key
* @return      long long Private key handle
*/
long long import_base64_prikey_handler(const char *buf, int buf_size);

/**
* @brief       The base64 encoding of the private key is exported
* @return      char* base64 encoding of the private key
*/
char *export_new_prikey_base64();

/**
* @brief       Generates the seed and returns the hexadecimal string of the seed
* @return      char* The hexadecimal string of seeds
*/
char *export_new_seed();

/**
* @brief       Pass in the hexadecimal encoding of the private key and return the private key handle
* @param       str: Hexadecimal encoding of the private key
* @return      long long Private key handle
*/
long long import_prikey_handler_from_hex(const char *str);

/**
* @brief       Gets the private key handle from the hexadecimal seed string
* @param       seed: 
* @return      long long 
*/
long long import_prikey_handler_from_seed(char *seed);

/**
* @brief       Pass the private key handle and return the hexadecimal code of the private key
* 
* @param       pkey: handle
* @return      char* Hexadecimal encoding of the private key
*/
char *export_new_prikey_to_hex(long long pkey);

/**
* @brief       Pass in seeds, return mnemonics
* @param       seed: seed
* @return      char* Private key handle
*/
char *export_mnemonic_from_seed(const char *seed);

/**
* @brief       Pass in seed mnemonics, return hexadecimal seeds
* @param       mnemonic: Seed mnemonics
* @return      char* seed
*/
char *import_seed_from_mnemonic(const char *mnemonic);

/**
* @brief       Pass the private key handle and return the addr account address of the private key
* @param       pkey: Private key handle
* @return      char* addr Account address
*/
char *get_addr(long long pkey);

/**
* @brief       Pass in the private key handle and return the base64 encoding of the public key
* @param       pkey: Private key handle
* @return      char* base64 encoding of the public key
*/
char *get_pubstr_base64(long long pkey);

/**
* @brief       Release the private key handle
* @param       pkey: Private key handle
*/
void free_prikey_handler(long long pkey);

/**
* @brief       Sign the resulting transaction returned by GetTransaction
* @param       message: "tx"json
* @param       msize: "tx"json length
* @param       pkey: Private key handle
* @return      char* Message after signature
*/
char *sig_tx(const char *message, int msize, long long pkey);


/**
* @brief       Sign the resulting transaction returned by GetTransaction
* @param       message: contract"tx"json
* @param       msize: contract"tx"json length
* @param       pkey: Private key handle
* @return      char* Message after signature
*/
char *sig_contract_tx(const char *message, int msize, long long pkey);
/**
* @brief	  Signature of message
* @param       message	Information to sign
* @param       mesage_size	Message length
* @param       pkey	Private key handle
* @return      char*	The message after the signature
*/
char *sign(const char *message, int mesage_size, long long pkey);


/**
* @brief       Sign "txJson" in the "result" field of the transaction return value
* @param       txjson: "txJson" message
* @param       pkey: Private key handle
* @return      char* Message after signature
*/
char* txJsonSign(const char* txjson, void *pkey);

/**
* @brief	  Check the information
* @param       pubstr	Public key
* @param       pubsize	Public key length
* @param       message	The message after the signature
* @param       messagesize	Length of the message after the signature
* @param       signature	Information to sign
* @param       signature_size The length of the message to sign
* @return      int	0 indicates success and -1 indicates failure
*/
int verif_by_public_str(const char *pubstr, int pubsize, const char *message, int messagesize, const char *signature, int signature_size);

```



### Android

```c
/**
* @brief	  Create hexadecimal seeds
* @return      jbyteArray : Hexadecimal seed
*/
JNIEXPORT jbyteArray JNICALL Java_com_example_jni_sig_newSeed
  (JNIEnv *env , jobject);


/**
* @brief	  Export the private key hexadecimal array based on the private key
* @param       jlong : Private key
* @return      jstring : Private key hexadecimal array
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_ExportPriHexStr
  (JNIEnv *, jobject, jlong);


/**
* @brief	  Export the private key from the private key hexadecimal array
* @param       jstring : Private key hexadecimal array
* @return      jlong : Private key
*/
JNIEXPORT jlong JNICALL Java_com_example_jni_sig_ImportPriHexStr
  (JNIEnv *, jobject, jstring);


/**
* @brief	  Export the private key from the private key hexadecimal array
* @param       jbyteArray : Private key hexadecimal array
* @return      jlong : Private key
*/
JNIEXPORT jlong JNICALL Java_com_example_jni_sig_importSeed
  (JNIEnv * env, jobject, jbyteArray str);


/**
* @brief	  Derive mnemonics from a hexadecimal array of seeds
* @param       jbyteArray : A hexadecimal array of seeds
* @return      jstring : Mnemonic word
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_ExportMnemoic
  (JNIEnv *, jobject, jbyteArray);

/**
* @brief	  A hexadecimal array of derived seeds based on mnemonics
* @param       jstring : Mnemonic word
* @return      jbyteArray : A hexadecimal array of seeds
*/
JNIEXPORT jbyteArray JNICALL Java_com_example_jni_sig_ImportMnemoic
  (JNIEnv *, jobject, jstring);


/**
* @brief	  Obtain the public key base64
* @param       jlong : Public key 
* @return      jstring : Public key base6
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_GetPubStr
  (JNIEnv *, jobject, jlong);


/**
* @brief	  Obtain the public key base64
* @param       jlong pkey: Public key 
* @return      jstring : Public key base6
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_GetContractPubStr
 (JNIEnv *env, jobject, jlong pkey);


/**
* @brief	  Get the address from the private key
* @param       jlong : Private key 
* @return      jstring : address
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_GetAddr
  (JNIEnv *, jobject, jlong);


/**
* @brief	  Sign on data
* @param       jlong : Private key
* @param       jstring : Data to be signed   
* @return      jstring : The signed data
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_sigmessage
    (JNIEnv *, jobject, jlong, jstring);


/**
* @brief	  Sign on data
* @param       jlong pkey : Private key
* @param       jstring message : Data to be signed
* @return      jstring : The signed data
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_sigMessage
        (JNIEnv *env, jobject, jlong pkey, jstring message);


/**
* @brief	  Verification signature
* @param       jlong : Private key
* @param       jstring : The message after the signature 
* @param       jstring : Visa inspection result
* @return      jboolean :  Check whether the visa is successful
*/
JNIEXPORT jboolean JNICALL Java_com_example_jni_sig_vefmessage
  (JNIEnv *, jobject, jlong, jstring, jstring);


/**
* @brief	  Sign "txJson" in the "result" field of the transaction return value
* @param       jlong : Private key
* @param       jstring : "txJson" message
* @return      jstring : Return the signed txjson
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_sigTx
  (JNIEnv *, jobject, jlong, jstring);


/**
* @brief	  Encrypts the base64 string
* @param       jstring : The base64 string to encrypt
* @return      jstring : Encrypted data
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_Base64Encode
  (JNIEnv *, jobject, jstring);


/**
* @brief	  Decrypt the encrypted base64 string
* @param       jstring : The base64 string to decrypt
* @return      jstring : Decrypted data
*/
JNIEXPORT jstring JNICALL Java_com_example_jni_sig_Base64Decode
  (JNIEnv *, jobject, jstring);


/**
* @brief	  Release private key
* @param       jlong pkey Private key
*/
JNIEXPORT void JNICALL Java_com_example_jni_sig_freePrikey
        (JNIEnv *env, jobject, jlong pkey);
```

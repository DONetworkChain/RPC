## Query class interface

### GetTransactionByHash

**Instructions**:

Get the transaction information according to the hash

**Argument**:

* id Transparent information
* jsonrpc  json version
* params argument
  * txHash Transaction hash

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Return value number
    * 0	success
    * -1   Transaction hash error
    * -2    Failed to parse transaction body
  * message Call information
  * tx Trading information (see Trading information description for details)

example

```json
//req
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{"txHash":"434026a97ff15f3519a95f3600c527d8b68cc72f279a4e36705b526900cbfbf0"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetTransactionByHash",
  "result": {
    "code": 0,
    "message": "success",
    "tx": {
      "Consensus": 7,
      "Type": "Tx",
      "data": {
        "TxInfo": {
          "BonusAddr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
          "InvestAmount": 1000000000000,
          "InvestType": "Normal"
        }
      },
      "identity": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f",
      "time": 1716775934685374,
      "txHash": "0x64e91e7fa9ce873a1891806ae1adcc0af98d38ff78660c8408ad9caa81c67495",
      "txType": 4,
      "utxo": {
        "multisign": [
          {
            "pub": "Hv7Z7SrYgnK9WGI0qZJJkCcDBVG5mYZlAN2fe0RsdEEIY3i9iAbRK+JtT+hxrv1+pWJeR3IdT/81Mx6TlAkkAg==",
            "sign": "Hv7Z7SrYgnK9WGI0qZJJkCcDBVG5mYZlAN2fe0RsdEEIY3i9iAbRK+JtT+hxrv1+pWJeR3IdT/81Mx6TlAkkAg=="
          }
        ],
        "owner": [
          "0xFFFc74b51BC5e75527fE5970D04355958dd3657C"
        ],
        "vin": {
          "prevout": {
            "hash": [
              "0x7dd57386b958cb7ad02170bd5c190e369c1694f596d524d2b2bfa5e1a55c253b"
            ]
          },
          "vinsign": [
            {
              "pub": "MCowBQYDK2VwAyEA+X/pIfbC/gTA+iuG5yoLn6AH90PFdko5gWfURmCYC90=",
              "sign": "eArBhLH2J24CjgE6SnPMV1/p+5Uqyuh2QwCwD7ldeqpJ63hPpcQ0n9CiNXh8CNPeKJNufduL1WjfDvqHymiZBA=="
            }
          ]
        },
        "vout": [
          {
            "addr": "VirtualInvest",
            "value": 1000000000000
          },
          {
            "addr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
            "value": 6998899999939100
          },
          {
            "addr": "VirtualBurnGas",
            "value": 32400
          }
        ]
      },
      "verifySign": [
        {
          "pub": "MCowBQYDK2VwAyEAHDoLfSX+ygmvSICr/1Q/UnfLlPFkAQBB4oPZne/SoVo=",
          "sign": "bCoIyAR1qH5LDHpX5Y5E5OqZogQo0EDDPnihTaPDHV5jQdT9AEadCo/+uhRMOi7l9XlwxhrCcxesnfJDXbQmCg==",
          "signaddr": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f"
        },
        {
          "pub": "MCowBQYDK2VwAyEABK13LqOyxq7skjywUZwpTTLVXU3yPMSClL0u9xI5+hg=",
          "sign": "",
          "signaddr": "0x2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5"
        },
        {
          "pub": "MCowBQYDK2VwAyEANFAhkjOUKAp0RbqjjiDetKQjcwQTXLRpL0Vh7uz3Sm0=",
          "sign": "",
          "signaddr": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2"
        },
        {
          "pub": "MCowBQYDK2VwAyEAl0V//ZTw/56RkIUtrEzyXIbPm0nQ+XjB2QEDZR+KbT4=",
          "sign": "",
          "signaddr": "0x3CA9403151e5E7ad6072c9CF29237A3BB61eFaF3"
        },
        {
          "pub": "MCowBQYDK2VwAyEAtLhQrLNMMCWqjBzgy3cf/eRC7ypLgZgg7inzrFP4vyY=",
          "sign": "",
          "signaddr": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95"
        },
        {
          "pub": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
          "sign": "",
          "signaddr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F"
        },
        {
          "pub": "MCowBQYDK2VwAyEACPZP4VDg6AE4zXC3GN0et49O0wxAQ5bNfgqDulRc+vk=",
          "sign": "",
          "signaddr": "0x244125ddD7A63479F3A5DA8bC36682EdaFfdc92d"
        },
        {
          "pub": "MCowBQYDK2VwAyEAdTGsapuDIoqcgqXHYKJgNPuTkwhZ6EYGi9ORPXV7krQ=",
          "sign": "",
          "signaddr": "0xca3B60adeEf20337427b0d4Fa6E62920ea81a855"
        },
        {
          "pub": "MCowBQYDK2VwAyEAh6RFUhVdsoE3MehHfFNlj4tWgyzLo+8F6SIPbW7zIYw=",
          "sign": "",
          "signaddr": "0x28bA6E30cB0d9372a18c80552eE11DFe47883FAd"
        },
        {
          "pub": "MCowBQYDK2VwAyEAZVRP0epGewUhFeh7p6tvzX3Rhn4BSB/7Exjqr8hW5yk=",
          "sign": "",
          "signaddr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169"
        },
        {
          "pub": "MCowBQYDK2VwAyEANkIfPzXigAr1hfIIh4qaJ7bG0jrC7a5F1FUR39kBnoE=",
          "sign": "",
          "signaddr": "0x08C08F389c8255c0B4d1C5e337C811D02F220B6e"
        },
        {
          "pub": "MCowBQYDK2VwAyEAQ05ytVs7kiZxfN2f6PUT9XpjfASpuMxoDNTJkzmimew=",
          "sign": "",
          "signaddr": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F"
        },
        {
          "pub": "MCowBQYDK2VwAyEAE9q3hlengBKro4iPMtj+F3RGyoJ7DdyToMzBSFvv2f8=",
          "sign": "",
          "signaddr": "0x1A2a22101480Cd3c0f966e0399cc5f4150B0EbF7"
        }
      ]
    }
  }
}
```

### GetBlockByTransactionHash

**Instructions**:

Get block information based on the transaction hash

**Argument**:

* id Transparent information
* jsonrpc  json version
* params argument
  * txHash Transaction hash

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Return value number
    * 0	success
    * -1   Tx hash error
    * -2   Block hash error
    * -3   block_raw parse fail!
    * -4   Block invert error
  * message Call information
  * blockInfo Block information (see Block information description for details)

example

```json
//req
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{"txHash":"0x76c975e7ce1591b920d10438dd39fa95d48e7c8dd6f730c68ead0aceda9ab2a9"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBlockByTransactionHash",
  "result": {
    "blockInfo": {
      "block": {
        "blocksign": [
          {
            "pub": "MCowBQYDK2VwAyEAae/Wg3GgmSC25Wl58xBvX3mCc+RWj9bcKkz5x/DfomU=",
            "sign": "33M7oPV1w50svBRFKw8EE5UVzd5uBMf87/FKakM4BkVz46iroxdxR8kNzD7gK1F1br60q15sIqTy+QlyQKSVAA==",
            "signaddr": "0x1C67D66a221A799b286a37182EC95A4e3817EB6e"
          },
          {
            "pub": "MCowBQYDK2VwAyEAWzv0JeQr3NcJbDBgV/9nsDT0xW5q9psR7I6CoJdIDYg=",
            "sign": "KTHmQYbvz+ZDjjOR5/kEsfWUHP+KmIrNJOpWdAm9+y6DJLydNJc4aTvJsCU/8qt9GJK2JCK/GgKR+hC4FMxIAQ==",
            "signaddr": "0x98C78D04c1740d54073e3CeD34Fa90c06dc71c66"
          },
          {
            "pub": "MCowBQYDK2VwAyEA8LDWKq+sDaT1c2OZqBFn4i2JGqCqFI+uQLOu81RAufI=",
            "sign": "fTBTe+sv+jCTmL4vMu0FZRHywB8xEW3VqX/x40Z4Y2TRa9qcxZ/toTzRw1YmO3fYlQQ7SC4qVr9MAKHnnzBUDA==",
            "signaddr": "0x66224D2cbA42e71de4fE1F450eE72DA013282F43"
          },
          {
            "pub": "MCowBQYDK2VwAyEAhjm7+MQ4K0YsaV03hIm8fmOZPxDR0e8tbvsW1DvcaKg=",
            "sign": "EI2Ffyg9QY+RA9PjpWhCzszOkm3utD0K9NC5qg8M6FbRrWvnJGPzkzr/E6UyfSXG/semq96JA5KM4XbCyMemDQ==",
            "signaddr": "0x11955a6D63740bF443BF8C45c6f81bD5b75Ad829"
          },
          {
            "pub": "MCowBQYDK2VwAyEA7jjEM/N3WCQpwQQjNJCBDnuWBVDDiGJaOLVnG9qmF0c=",
            "sign": "6cOipr6o8lJb3k4Ha5KfCiZGGL2pC7W+eZVsYYses8GJAxOI0h9Ut559KGVf/igeqNfOx5tAITKApwyBWhMiBw==",
            "signaddr": "0x93c8fc833250210f9d4293a9D05D5BCb7580a12b"
          },
          {
            "pub": "MCowBQYDK2VwAyEAgAZhAMP7Runy+kuMxm+njbAyLMvqJ+TkMztoIoz67cM=",
            "sign": "jb/TD52Z3KWK7UvP0Mr4k3D8ZXwhE0TOfD7zU0JIw/yk/KqSv1ePpAg1glFok7bAIQhJ4UMVbySGwZc8a0CWDg==",
            "signaddr": "0x5E001f35dd385AF51c5F1f5F7Ebd433dA3f6c50b"
          },
          {
            "pub": "MCowBQYDK2VwAyEAitOB3dF8VudtN4+JvMAYp6CpqouvYrDy8V1Hcr1wO/8=",
            "sign": "8oT5zVLq6NMsF96nGN+X4yR2O28z35xyEc+fd0k2Owid2bUAI3alqQ553jahm29aAEsMntBwQfEWJru2fIfsAw==",
            "signaddr": "0xaD09de6F0e09eba0CB54198f34b908D53dDD47C2"
          }
        ],
        "bytes": 2358,
        "data": null,
        "hash": "0x6e7516748906bf011f4137247b2563c2ab1b964b39537eb062d28179f191cf6c",
        "height": 10,
        "merkleroot": "0x76c975e7ce1591b920d10438dd39fa95d48e7c8dd6f730c68ead0aceda9ab2a9",
        "prevhash": "0x80378d38d7266a9a03a7992524a94c92f81eb395a789b0f66e1a6bf9afde9c92",
        "time": 1726728006313484
      },
      "tx": [
        {
          "Consensus": 7,
          "Type": "Tx",
          "data": {
            "TxInfo": {
              "CommissionRate": 0.06,
              "StakeAmount": 200000000000,
              "StakeType": "Net"
            }
          },
          "identity": "0x1C67D66a221A799b286a37182EC95A4e3817EB6e",
          "info": "MQ==",
          "time": 1726728005523207,
          "txHash": "0x76c975e7ce1591b920d10438dd39fa95d48e7c8dd6f730c68ead0aceda9ab2a9",
          "txType": 2,
          "utxo": {
            "multisign": [
              {
                "pub": "MCowBQYDK2VwAyEAae/Wg3GgmSC25Wl58xBvX3mCc+RWj9bcKkz5x/DfomU=",
                "sign": "qUTzE97cJeg+lkwchIRTg+9hEDPg6CT6+NMuW0cUZaxnvvFcAsLpAFSk3KqamVCj4Bw7vG1DK8cOPlf4YPYBCQ=="
              }
            ],
            "owner": [
              "0x1C67D66a221A799b286a37182EC95A4e3817EB6e"
            ],
            "vin": {
              "prevout": {
                "hash": [
                  "0x66b40f5fd923d98de76aff01f81b28b5fe4aba75f018b2a8f22962a21e25e1b9"
                ]
              },
              "vinsign": [
                {
                  "pub": "MCowBQYDK2VwAyEAae/Wg3GgmSC25Wl58xBvX3mCc+RWj9bcKkz5x/DfomU=",
                  "sign": "kLRwezL1tSUZayS7iruLxp1hskn8881Q8cHeTuxVuPo8TKNgOHX5OgSOvCz259cZ5Od/qmXniM5BgtYR6VXJCw=="
                }
              ]
            },
            "vout": [
              {
                "addr": "VirtualStake",
                "value": 200000000000
              },
              {
                "addr": "0x1C67D66a221A799b286a37182EC95A4e3817EB6e",
                "value": 2799999971500
              },
              {
                "addr": "VirtualBurnGas",
                "value": 28500
              }
            ]
          },
          "verifySign": [
            {
              "pub": "MCowBQYDK2VwAyEAae/Wg3GgmSC25Wl58xBvX3mCc+RWj9bcKkz5x/DfomU=",
              "sign": "CUHvre2wgded4iGZ3nGAI0Gokc/XTkoUgB6sauGQmUrHPgF0TJX/1YAkGP3+qeTE3ljrikXYEUE4Uk3sRLilAw==",
              "signaddr": "0x1C67D66a221A799b286a37182EC95A4e3817EB6e"
            },
            {
              "pub": "MCowBQYDK2VwAyEAMzrGlIWtPofhwDPSze8InqhrzkBcl9Z6C7biRMdVLQU=",
              "sign": "",
              "signaddr": "0x9886c3459d0680a952d42a99D34bE409Dc954EF4"
            },
            {
              "pub": "MCowBQYDK2VwAyEAOrkFVLU7YGA73AsaK3JeIcSVfWNzL77JXSoNUezbtcE=",
              "sign": "",
              "signaddr": "0xb8d41cCf02E44aDf146a9137300A5eAB04268cE3"
            },
            {
              "pub": "MCowBQYDK2VwAyEA7jjEM/N3WCQpwQQjNJCBDnuWBVDDiGJaOLVnG9qmF0c=",
              "sign": "",
              "signaddr": "0x93c8fc833250210f9d4293a9D05D5BCb7580a12b"
            },
            {
              "pub": "MCowBQYDK2VwAyEAVxOzHxZcOh6M21xbNPZOtG0iGEamiUxdYZ0ZTUYaGdc=",
              "sign": "",
              "signaddr": "0xa4D07C108aD7eA5B7dA232F662Fc37e0FF7CF293"
            },
            {
              "pub": "MCowBQYDK2VwAyEAPQySWDAp2DflT7aZwpcF1L4zItDvdnV3Wz+FSOdVho4=",
              "sign": "",
              "signaddr": "0xce673F0d3C8441460c2107E66847DEa19623a697"
            },
            {
              "pub": "MCowBQYDK2VwAyEABP1wDUhjbpeXfLMKFao4kefn0kEgA3aUItxpvM6WF1w=",
              "sign": "",
              "signaddr": "0x20Afe2b661446a33EE8cEE8f6ce0c1AdEdbBF03C"
            },
            {
              "pub": "MCowBQYDK2VwAyEAitOB3dF8VudtN4+JvMAYp6CpqouvYrDy8V1Hcr1wO/8=",
              "sign": "",
              "signaddr": "0xaD09de6F0e09eba0CB54198f34b908D53dDD47C2"
            },
            {
              "pub": "MCowBQYDK2VwAyEAWzv0JeQr3NcJbDBgV/9nsDT0xW5q9psR7I6CoJdIDYg=",
              "sign": "",
              "signaddr": "0x98C78D04c1740d54073e3CeD34Fa90c06dc71c66"
            },
            {
              "pub": "MCowBQYDK2VwAyEAgAZhAMP7Runy+kuMxm+njbAyLMvqJ+TkMztoIoz67cM=",
              "sign": "",
              "signaddr": "0x5E001f35dd385AF51c5F1f5F7Ebd433dA3f6c50b"
            },
            {
              "pub": "MCowBQYDK2VwAyEA8LDWKq+sDaT1c2OZqBFn4i2JGqCqFI+uQLOu81RAufI=",
              "sign": "",
              "signaddr": "0x66224D2cbA42e71de4fE1F450eE72DA013282F43"
            },
            {
              "pub": "MCowBQYDK2VwAyEAhjm7+MQ4K0YsaV03hIm8fmOZPxDR0e8tbvsW1DvcaKg=",
              "sign": "",
              "signaddr": "0x11955a6D63740bF443BF8C45c6f81bD5b75Ad829"
            },
            {
              "pub": "MCowBQYDK2VwAyEA53pJcb452ziFkBVb8APZuoo24SjA8ddO8Jj/v+WRAYY=",
              "sign": "",
              "signaddr": "0x8Af11633a1a93b0030d13117DF9e3A3aF57F3972"
            }
          ]
        }
      ]
    },
    "code": 0,
    "message": "success"
  }
}

```

### GetBlockByHash

**Instructions**:

Get block information based on block hash

**Argument**:

* id Transparent information
* jsonrpc  json version
* params argument
  * blockHash Block hash

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Return value number
    * 0	success
    * -1   Block hash error
  * message Call information
  * blockInfo Block information (see Block information description for details)

example

```json
//req
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{"blockHash":"139009febd771d3f0d49d0ec179a8706e362af48a989dcfededb4aa2a18aaa08"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBlockByHash",
  "result": {
    "blockInfo": {
      "block": {
        "blocksign": [
          {
            "pub": "MCowBQYDK2VwAyEAvU/OXGoLVyRBFQe8V9FuD9xDVsTMhIkF6MQjCQjeaX4=",
            "sign": "wL1MIpdaX1n6jwmt+Vt7NF+emCsCVkT1aOAw0jv2mhLMe3g4t1c/dNQ0zUBZWsbhnDDwIi7g30fG9S6ryanyAw==",
            "signaddr": "0x116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2"
          },
          {
            "pub": "MCowBQYDK2VwAyEANFAhkjOUKAp0RbqjjiDetKQjcwQTXLRpL0Vh7uz3Sm0=",
            "sign": "k469bWQ4LbkjpPtFIdIRbEaTCxIWm9PuSIypd47QbjrZW5FojwIs2cZi9pMbkVK+D6VGvmcG1jOPjw8WbUMTCg==",
            "signaddr": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2"
          },
          {
            "pub": "MCowBQYDK2VwAyEAawp+8tDyeSREnNHrEaeBs6B9AeclJOlrAkeWMijTPww=",
            "sign": "CbveF6sEvQB9nGCLXg3NQ9wQidV+Ia18wDFnKdKK8fPuB59BRI9KmdEejr64QG5cZEpnYn0MUC4x5xfCLSEQAg==",
            "signaddr": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9"
          },
          {
            "pub": "MCowBQYDK2VwAyEApakW/x/DvV7BBRmhbQzkxhj7xbS0Xr5JN4tSEigWshA=",
            "sign": "IJ0131I2VWKDa8WqPYfmeFt4Zif8Tc9s6qFg/+fXbs3HUBjj/CPLT1+R1zQ6GbDp2OcmU9+/8w/6dJgcn0DCBw==",
            "signaddr": "0x8C33DF5ca4a4de15B53316dc3db60Ae4A7e09734"
          },
          {
            "pub": "MCowBQYDK2VwAyEAkHwtzRc4cHtDid6kE/hqO/h6bPlU+cG5ZigBEwOGD2Y=",
            "sign": "Qjhe+YtgfciStNLe8dzf6mHue7U6ydcaNfBayNcQP/vfvVovVsrVXcKLdvnvEdgIioRV44ZF/BWDQJXXSBQtCA==",
            "signaddr": "0xB6AE1C10C5547ed1D6ba50d74cc92214E17b5111"
          },
          {
            "pub": "MCowBQYDK2VwAyEAQ05ytVs7kiZxfN2f6PUT9XpjfASpuMxoDNTJkzmimew=",
            "sign": "7KlsOLj31R5hAbJXIlB8pJIG3E2Ubir9CE84sz8RuB8hhdPmLUgWZHUmdI25OtQYhN926N26bz1WwxOqURj3Dw==",
            "signaddr": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F"
          },
          {
            "pub": "MCowBQYDK2VwAyEA+X/pIfbC/gTA+iuG5yoLn6AH90PFdko5gWfURmCYC90=",
            "sign": "X3TlGlovnPUSsI6ojA4/PyY05XSxLJmBxiDzmbcjHgyxhrvCovZ6F7zi+GkKHIgMYwDmGL16nkbhu2oXyLIWBQ==",
            "signaddr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C"
          }
        ],
        "bytes": 2399,
        "data": {
          "dependentCTx": ""
        },
        "hash": "0x139009febd771d3f0d49d0ec179a8706e362af48a989dcfededb4aa2a18aaa08",
        "height": 541,
        "merkleroot": "0x434026a97ff15f3519a95f3600c527d8b68cc72f279a4e36705b526900cbfbf0",
        "prevhash": "0x96c1691d58d2cbec05eaf8792b2cd58fbbea0aad19ad3daf27b665fb5886f33c",
        "time": 1716796707667741
      },
      "tx": [
        {
          "Consensus": 7,
          "Type": "Tx",
          "data": {
            "TxInfo": {
              "BonusAddr": "0x855052fa258B463AEAd1E5abD55F2ffbCBb3F022",
              "InvestAmount": 1000000000000,
              "InvestType": "Normal"
            }
          },
          "identity": "0x116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2",
          "info": "MQ==",
          "time": 1716796705692762,
          "txHash": "0x434026a97ff15f3519a95f3600c527d8b68cc72f279a4e36705b526900cbfbf0",
          "txType": 4,
          "utxo": {
            "multisign": [
              {
                "pub": "scIqQ/SPPhUc2egQgpEL21qk/NcnoH//xOv5h8M1hSXUGAM3CuitY1FEPI0QtRvXV5hmcajQlWDEDJ3bQDjVCg==",
                "sign": "scIqQ/SPPhUc2egQgpEL21qk/NcnoH//xOv5h8M1hSXUGAM3CuitY1FEPI0QtRvXV5hmcajQlWDEDJ3bQDjVCg=="
              }
            ],
            "owner": [
              "0x855052fa258B463AEAd1E5abD55F2ffbCBb3F022"
            ],
            "vin": {
              "prevout": {
                "hash": [
                  "0x7637b67f47793d4bb9b017ead8d987971516e5b49a1073c8c6691f1e12c7ad6a"
                ]
              },
              "vinsign": [
                {
                  "pub": "MCowBQYDK2VwAyEAwigpWZg9E0DRbbbNuE4PDHT7MJ9XIH2hh5yADHNa6jw=",
                  "sign": "wsdl+IJJ8aaC3q/em5cmUidQllESaePErugQT2xeUdRtohw7PQmi0X899BgZZE1sh8rhYnCC68kf19Y9W+ykAg=="
                }
              ]
            },
            "vout": [
              {
                "addr": "VirtualInvest",
                "value": 1000000000000
              },
              {
                "addr": "0x855052fa258B463AEAd1E5abD55F2ffbCBb3F022",
                "value": 1899998701374
              },
              {
                "addr": "VirtualBurnGas",
                "value": 32400
              }
            ]
          },
          "verifySign": [
            {
              "pub": "MCowBQYDK2VwAyEAvU/OXGoLVyRBFQe8V9FuD9xDVsTMhIkF6MQjCQjeaX4=",
              "sign": "yLr5Zft97qilx6KUPopmWwgVUG5WBG+rxU6gH+DtMKXNQkO7Fm+3/y3gAohj9UPhf7ECI+fTKczUz35tjC+/Bg==",
              "signaddr": "0x116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2"
            },
            {
              "pub": "MCowBQYDK2VwAyEAh6RFUhVdsoE3MehHfFNlj4tWgyzLo+8F6SIPbW7zIYw=",
              "sign": "",
              "signaddr": "0x28bA6E30cB0d9372a18c80552eE11DFe47883FAd"
            },
            {
              "pub": "MCowBQYDK2VwAyEAd2sNbj9c8IKcU8zzC2qWrGkwwFkZSQTtkvrgkxCzpTE=",
              "sign": "",
              "signaddr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b"
            },
            {
              "pub": "MCowBQYDK2VwAyEAB13mSe2XJ46JzM6WC3sOh7dh5TlMaDevNUlX7b4tuu8=",
              "sign": "",
              "signaddr": "0xD82a5740De434f67b64946ba5939dfECc594Bcc1"
            },
            {
              "pub": "MCowBQYDK2VwAyEANFAhkjOUKAp0RbqjjiDetKQjcwQTXLRpL0Vh7uz3Sm0=",
              "sign": "",
              "signaddr": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2"
            },
            {
              "pub": "MCowBQYDK2VwAyEAQ05ytVs7kiZxfN2f6PUT9XpjfASpuMxoDNTJkzmimew=",
              "sign": "",
              "signaddr": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F"
            },
            {
              "pub": "MCowBQYDK2VwAyEApakW/x/DvV7BBRmhbQzkxhj7xbS0Xr5JN4tSEigWshA=",
              "sign": "",
              "signaddr": "0x8C33DF5ca4a4de15B53316dc3db60Ae4A7e09734"
            },
            {
              "pub": "MCowBQYDK2VwAyEAawp+8tDyeSREnNHrEaeBs6B9AeclJOlrAkeWMijTPww=",
              "sign": "",
              "signaddr": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9"
            },
            {
              "pub": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
              "sign": "",
              "signaddr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F"
            },
            {
              "pub": "MCowBQYDK2VwAyEAl0V//ZTw/56RkIUtrEzyXIbPm0nQ+XjB2QEDZR+KbT4=",
              "sign": "",
              "signaddr": "0x3CA9403151e5E7ad6072c9CF29237A3BB61eFaF3"
            },
            {
              "pub": "MCowBQYDK2VwAyEA+X/pIfbC/gTA+iuG5yoLn6AH90PFdko5gWfURmCYC90=",
              "sign": "",
              "signaddr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C"
            },
            {
              "pub": "MCowBQYDK2VwAyEAkHwtzRc4cHtDid6kE/hqO/h6bPlU+cG5ZigBEwOGD2Y=",
              "sign": "",
              "signaddr": "0xB6AE1C10C5547ed1D6ba50d74cc92214E17b5111"
            },
            {
              "pub": "MCowBQYDK2VwAyEAcUcydwF7CSr9bjBiUbd3drV+WMd4yd8xFL7HWGA4FTw=",
              "sign": "",
              "signaddr": "0x9234e37d86AE7De3Dd0Ac57AF815b54551873504"
            }
          ]
        }
      ]
    },
    "code": 0,
    "message": "success"
  }
}
```

### GetBlockByHeight

**Instructions**:

Get block information based on block height

**Argument**:

* id Transparent information
* jsonrpc  json version
* params argument
  * beginHeight Starting block height
  * endHeight End block height
  * If endHeight > top, endHeight = top, and the difference between beginHeight and endHeight is 100 at most

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    * 0	success
    * -1   Block height error, beginHeight < endHeight
    * -2   The height of the request does not exceed 100
    * -3    Database abnormal, Get block hashes by block height error
    * -4    Database abnormal, Get block by block hash error
    * -5    Database abnormal, Get block top error
  * message Call information
  * blocks Block information (see Block information description for details)

example

```json
//req
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{"beginHeight":"2484", "endHeight":"2584"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBlockByHeight",
  "result": {
    "blocks": [
      {
        "block": {
          "blocksign": [
            {
              "pub": "MCowBQYDK2VwAyEAYc23TU7Tw6L9QcUXNM6FuS5kEzTTQEfX15dR9+n251Y=",
              "sign": "nYmcHtPifKAydKyaP8UOhfyPsxLfUg4cscFx4aW8BdGp0MzBnJGajgrYr35QY2QGMh8KSsldcjwqaDP1t4aZAA==",
              "signaddr": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce"
            },
            {
              "pub": "MCowBQYDK2VwAyEAawp+8tDyeSREnNHrEaeBs6B9AeclJOlrAkeWMijTPww=",
              "sign": "S76VLYxJM6FhhiKsQqMlgaNIkeq/cutG+Zzdrd6+UWcuIDsDBHSzIzO8WO4D3UPswFQdejMW6KRkz2AbLdgFAg==",
              "signaddr": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9"
            },
            {
              "pub": "MCowBQYDK2VwAyEAbA5Gq2olxI11gecRsyYYmaecJN0ht74mB2fLNWb3TcQ=",
              "sign": "/raN6bn34kGADpGTFevp2kZ7TSwq+Wv2OtqKXdG0hH9g8DapxmAnIkx6+QW6trdesIOrmK4Qv6mF37VuA23TCQ==",
              "signaddr": "0x8F66e288547032026dd1ddFb992ff7eEcD9261f0"
            },
            {
              "pub": "MCowBQYDK2VwAyEAnkb8f/5s/LsQXNlU7/SDXR2sPf8IZZrbZ9v2HmYJffk=",
              "sign": "o39g5WRolJaEvkuvKv0B8jgV8qQ/HUJdnmTiXjS7DXMLCb9bLbRGjdSHcmGEXR1XiRJnNo7iuW2BaMUtZLA0CQ==",
              "signaddr": "0x01921896D8AAC12B19BC8413135907AB5aE82326"
            },
            {
              "pub": "MCowBQYDK2VwAyEAtLhQrLNMMCWqjBzgy3cf/eRC7ypLgZgg7inzrFP4vyY=",
              "sign": "pNDOOGK0Raa5/VuEoTKOkJzPUluPH26SzXHQPthwcwp8ZmigtOGpsH7MpgPZSPVByb0kIZoEtTqF2jJdllksDw==",
              "signaddr": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95"
            },
            {
              "pub": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
              "sign": "NWBgjHQNSpVr7lFtNh6W+qe2XgDRH7Jd/ZI7cunHrRy0kbGFHjaHbX7USg3J0a8tpfviKPG4S7v5KMyAu2MsAQ==",
              "signaddr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F"
            },
            {
              "pub": "MCowBQYDK2VwAyEAd2sNbj9c8IKcU8zzC2qWrGkwwFkZSQTtkvrgkxCzpTE=",
              "sign": "SsuX3d8C0CY2FzsSWfQn/bhlIXEHGnKugsCcYYKu5oV0alZJFpcsjKVADSy2/qRX4Ww6BcfGVEBIOvJnrYCgAQ==",
              "signaddr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b"
            }
          ],
          "bytes": 2398,
          "data": {
            "dependentCTx": ""
          },
          "hash": "0x85b85a2b88a9c993f44c21f45e43ff537eacfe08257d913ac9adcda223d14d4c",
          "height": 2484,
          "merkleroot": "0x446bd7acc5487883475b2c581f0c343bd9630adc35c88b584a52d5a2faec7ce8",
          "prevhash": "0xd0e8f63a7479df2cec92c701b4650eff8fbb31af6dba955f426b6966ea4541da",
          "time": 1717401536067676
        },
        "tx": [
          {
            "Consensus": 7,
            "Type": "Tx",
            "data": {
              "TxInfo": {
                "BonusAddr": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce",
                "InvestAmount": 800000000000,
                "InvestType": "Normal"
              }
            },
            "identity": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce",
            "info": "MQ==",
            "time": 1717401535678450,
            "txHash": "0x446bd7acc5487883475b2c581f0c343bd9630adc35c88b584a52d5a2faec7ce8",
            "txType": 4,
            "utxo": {
              "multisign": [
                {
                  "pub": "agc3qfYFfCGRHMJLSm/M37b32hITmFbt0VokGeECaEKazDrrUVDvwmRHY7QH/6lNMuuCVyfebhSjUr3AXW1ECg==",
                  "sign": "agc3qfYFfCGRHMJLSm/M37b32hITmFbt0VokGeECaEKazDrrUVDvwmRHY7QH/6lNMuuCVyfebhSjUr3AXW1ECg=="
                }
              ],
              "owner": [
                "0x638c172F63db3caf32c410D0188143E0Eff74bC8"
              ],
              "vin": {
                "prevout": {
                  "hash": [
                    "0xd738eaacbba575fff85f12d356bba157ff6dc1fcdf6c470ddf4d15cca26db7c5"
                  ]
                },
                "vinsign": [
                  {
                    "pub": "MCowBQYDK2VwAyEA878WPUVdMcjoPM+ZI1qC59e8nLgNXi/MAGIRFyU0kPM=",
                    "sign": "4H63JOxLz7T4ZxLaVAd3VMS3JUCAfv1blpaNVOM8vFyKrkk5NULHay5unpWlXQjIDEjOJCWo9jttJsoBXJbhBw=="
                  }
                ]
              },
              "vout": [
                {
                  "addr": "VirtualInvest",
                  "value": 800000000000
                },
                {
                  "addr": "0x638c172F63db3caf32c410D0188143E0Eff74bC8",
                  "value": 2199999967700
                },
                {
                  "addr": "VirtualBurnGas",
                  "value": 32300
                }
              ]
            },
            "verifySign": [
              {
                "pub": "MCowBQYDK2VwAyEAYc23TU7Tw6L9QcUXNM6FuS5kEzTTQEfX15dR9+n251Y=",
                "sign": "5+excKFT9ZgiLS12P2zrRzy565esiAtckqcFpsjWHY/6gWAJv6++5m9mn+P5eRhK8kU2iBGS4cIY7+lxadWiAA==",
                "signaddr": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce"
              },
              {
                "pub": "MCowBQYDK2VwAyEAZVRP0epGewUhFeh7p6tvzX3Rhn4BSB/7Exjqr8hW5yk=",
                "sign": "",
                "signaddr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169"
              },
              {
                "pub": "MCowBQYDK2VwAyEAvU/OXGoLVyRBFQe8V9FuD9xDVsTMhIkF6MQjCQjeaX4=",
                "sign": "",
                "signaddr": "0x116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2"
              },
              {
                "pub": "MCowBQYDK2VwAyEAtLhQrLNMMCWqjBzgy3cf/eRC7ypLgZgg7inzrFP4vyY=",
                "sign": "",
                "signaddr": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95"
              },
              {
                "pub": "MCowBQYDK2VwAyEAawp+8tDyeSREnNHrEaeBs6B9AeclJOlrAkeWMijTPww=",
                "sign": "",
                "signaddr": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9"
              },
              {
                "pub": "MCowBQYDK2VwAyEAd2sNbj9c8IKcU8zzC2qWrGkwwFkZSQTtkvrgkxCzpTE=",
                "sign": "",
                "signaddr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b"
              },
              {
                "pub": "MCowBQYDK2VwAyEACPZP4VDg6AE4zXC3GN0et49O0wxAQ5bNfgqDulRc+vk=",
                "sign": "",
                "signaddr": "0x244125ddD7A63479F3A5DA8bC36682EdaFfdc92d"
              },
              {
                "pub": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
                "sign": "",
                "signaddr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F"
              },
              {
                "pub": "MCowBQYDK2VwAyEAz7Y+YE+zTAZO26NcyvbWFpwPOYS18kyofL9pitE73G0=",
                "sign": "",
                "signaddr": "0x3292FEAbea61A76cf59Fa917b9DCcC937Ca489eE"
              },
              {
                "pub": "MCowBQYDK2VwAyEABK13LqOyxq7skjywUZwpTTLVXU3yPMSClL0u9xI5+hg=",
                "sign": "",
                "signaddr": "0x2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5"
              },
              {
                "pub": "MCowBQYDK2VwAyEAnkb8f/5s/LsQXNlU7/SDXR2sPf8IZZrbZ9v2HmYJffk=",
                "sign": "",
                "signaddr": "0x01921896D8AAC12B19BC8413135907AB5aE82326"
              },
              {
                "pub": "MCowBQYDK2VwAyEAbA5Gq2olxI11gecRsyYYmaecJN0ht74mB2fLNWb3TcQ=",
                "sign": "",
                "signaddr": "0x8F66e288547032026dd1ddFb992ff7eEcD9261f0"
              },
              {
                "pub": "MCowBQYDK2VwAyEAner1iR+SqRLmN0lLWB0+su0Quh0XpNDTmm9PWWODirI=",
                "sign": "",
                "signaddr": "0x8fFb06c288C30F3e62b31d6c5FD34328A964774a"
              }
            ]
          }
        ]
      }
    ],
    "code": 0,
    "message": "success"
  }
}
```

### ConfirmTransaction

Confirm whether the transaction is on the chain

**Argument**

- txhash Transaction hash
- Trading height

**Returned value**:

- code Return value number
  - 0 success
  - -1 Nodelist size is empty
  - -2 FilterHeightNodeList size is empty
  - -3 CreateWait error
  - -4 AddResNode error
  - -5 WaitData error
  - -6 susSize node list is empty
  - -7 The amount received was too small to verify transaction on-chain
  - -8 tx Parse error

- message Return value information
- tx Transaction body information
- percent On-chain rate
- sendsize Number of request nodes
- receivedsize The number of replies received

```json
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{
      "txhash":"64e91e7fa9ce873a1891806ae1adcc0af98d38ff78660c8408ad9caa81c67495",
      "height": "500"
    }
}
```

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "ConfirmTransaction",
  "result": {
    "code": 0,
    "message": "success",
    "percent": "1.000000",
    "receivedsize": "27",
    "sendsize": "34",
    "tx": {
      "Consensus": 7,
      "Type": "Tx",
      "data": {
        "TxInfo": {
          "BonusAddr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
          "InvestAmount": 1000000000000,
          "InvestType": "Normal"
        }
      },
      "identity": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f",
      "time": 1716775934685374,
      "txHash": "0x64e91e7fa9ce873a1891806ae1adcc0af98d38ff78660c8408ad9caa81c67495",
      "txType": 4,
      "utxo": {
        "multisign": [
          {
            "pub": "Hv7Z7SrYgnK9WGI0qZJJkCcDBVG5mYZlAN2fe0RsdEEIY3i9iAbRK+JtT+hxrv1+pWJeR3IdT/81Mx6TlAkkAg==",
            "sign": "Hv7Z7SrYgnK9WGI0qZJJkCcDBVG5mYZlAN2fe0RsdEEIY3i9iAbRK+JtT+hxrv1+pWJeR3IdT/81Mx6TlAkkAg=="
          }
        ],
        "owner": [
          "0xFFFc74b51BC5e75527fE5970D04355958dd3657C"
        ],
        "vin": {
          "prevout": {
            "hash": [
              "0x7dd57386b958cb7ad02170bd5c190e369c1694f596d524d2b2bfa5e1a55c253b"
            ]
          },
          "vinsign": [
            {
              "pub": "MCowBQYDK2VwAyEA+X/pIfbC/gTA+iuG5yoLn6AH90PFdko5gWfURmCYC90=",
              "sign": "eArBhLH2J24CjgE6SnPMV1/p+5Uqyuh2QwCwD7ldeqpJ63hPpcQ0n9CiNXh8CNPeKJNufduL1WjfDvqHymiZBA=="
            }
          ]
        },
        "vout": [
          {
            "addr": "VirtualInvest",
            "value": 1000000000000
          },
          {
            "addr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
            "value": 6998899999939100
          },
          {
            "addr": "VirtualBurnGas",
            "value": 32400
          }
        ]
      },
      "verifySign": [
        {
          "pub": "MCowBQYDK2VwAyEAHDoLfSX+ygmvSICr/1Q/UnfLlPFkAQBB4oPZne/SoVo=",
          "sign": "bCoIyAR1qH5LDHpX5Y5E5OqZogQo0EDDPnihTaPDHV5jQdT9AEadCo/+uhRMOi7l9XlwxhrCcxesnfJDXbQmCg==",
          "signaddr": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f"
        },
        {
          "pub": "MCowBQYDK2VwAyEABK13LqOyxq7skjywUZwpTTLVXU3yPMSClL0u9xI5+hg=",
          "sign": "",
          "signaddr": "0x2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5"
        },
        {
          "pub": "MCowBQYDK2VwAyEANFAhkjOUKAp0RbqjjiDetKQjcwQTXLRpL0Vh7uz3Sm0=",
          "sign": "",
          "signaddr": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2"
        },
        {
          "pub": "MCowBQYDK2VwAyEAl0V//ZTw/56RkIUtrEzyXIbPm0nQ+XjB2QEDZR+KbT4=",
          "sign": "",
          "signaddr": "0x3CA9403151e5E7ad6072c9CF29237A3BB61eFaF3"
        },
        {
          "pub": "MCowBQYDK2VwAyEAtLhQrLNMMCWqjBzgy3cf/eRC7ypLgZgg7inzrFP4vyY=",
          "sign": "",
          "signaddr": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95"
        },
        {
          "pub": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
          "sign": "",
          "signaddr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F"
        },
        {
          "pub": "MCowBQYDK2VwAyEACPZP4VDg6AE4zXC3GN0et49O0wxAQ5bNfgqDulRc+vk=",
          "sign": "",
          "signaddr": "0x244125ddD7A63479F3A5DA8bC36682EdaFfdc92d"
        },
        {
          "pub": "MCowBQYDK2VwAyEAdTGsapuDIoqcgqXHYKJgNPuTkwhZ6EYGi9ORPXV7krQ=",
          "sign": "",
          "signaddr": "0xca3B60adeEf20337427b0d4Fa6E62920ea81a855"
        },
        {
          "pub": "MCowBQYDK2VwAyEAh6RFUhVdsoE3MehHfFNlj4tWgyzLo+8F6SIPbW7zIYw=",
          "sign": "",
          "signaddr": "0x28bA6E30cB0d9372a18c80552eE11DFe47883FAd"
        },
        {
          "pub": "MCowBQYDK2VwAyEAZVRP0epGewUhFeh7p6tvzX3Rhn4BSB/7Exjqr8hW5yk=",
          "sign": "",
          "signaddr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169"
        },
        {
          "pub": "MCowBQYDK2VwAyEANkIfPzXigAr1hfIIh4qaJ7bG0jrC7a5F1FUR39kBnoE=",
          "sign": "",
          "signaddr": "0x08C08F389c8255c0B4d1C5e337C811D02F220B6e"
        },
        {
          "pub": "MCowBQYDK2VwAyEAQ05ytVs7kiZxfN2f6PUT9XpjfASpuMxoDNTJkzmimew=",
          "sign": "",
          "signaddr": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F"
        },
        {
          "pub": "MCowBQYDK2VwAyEAE9q3hlengBKro4iPMtj+F3RGyoJ7DdyToMzBSFvv2f8=",
          "sign": "",
          "signaddr": "0x1A2a22101480Cd3c0f966e0399cc5f4150B0EbF7"
        }
      ]
    },
    "txhash": "0x64e91e7fa9ce873a1891806ae1adcc0af98d38ff78660c8408ad9caa81c67495"
  }
}
```

### GetAllStakeNodeList

Get a list of pledge nodes

**Argument**

- None

**Returned value**

- code Return value number
  - 0 success
  - -1 peerlist is empty

- message Return value information
- version edition
- list Pledge list
- addr address
- ip   ip address
- identity Account public key
- logo Node logo
- name Node name 

```json
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{}
}
```

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetAllStakeNodeList",
  "result": {
    "code": 0,
    "list": {
      "list": [
        {
          "addr": "0x01921896D8AAC12B19BC8413135907AB5aE82326",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAnkb8f/5s/LsQXNlU7/SDXR2sPf8IZZrbZ9v2HmYJffk=",
          "ip": "192.168.1.86",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAHDoLfSX+ygmvSICr/1Q/UnfLlPFkAQBB4oPZne/SoVo=",
          "ip": "192.168.1.118",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x08C08F389c8255c0B4d1C5e337C811D02F220B6e",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEANkIfPzXigAr1hfIIh4qaJ7bG0jrC7a5F1FUR39kBnoE=",
          "ip": "192.168.1.99",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAtLhQrLNMMCWqjBzgy3cf/eRC7ypLgZgg7inzrFP4vyY=",
          "ip": "192.168.1.95",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAd2sNbj9c8IKcU8zzC2qWrGkwwFkZSQTtkvrgkxCzpTE=",
          "ip": "192.168.1.100",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x1A2a22101480Cd3c0f966e0399cc5f4150B0EbF7",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAE9q3hlengBKro4iPMtj+F3RGyoJ7DdyToMzBSFvv2f8=",
          "ip": "192.168.1.104",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x1CD6855FB33190754b122f8aBad737791BaB3F0a",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAF/4cPYBHTbG05HVOwUSmM/0wWPdrf7UbB1VO2ZfDuK0=",
          "ip": "192.168.1.61",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x244125ddD7A63479F3A5DA8bC36682EdaFfdc92d",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEACPZP4VDg6AE4zXC3GN0et49O0wxAQ5bNfgqDulRc+vk=",
          "ip": "192.168.1.102",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x28bA6E30cB0d9372a18c80552eE11DFe47883FAd",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAh6RFUhVdsoE3MehHfFNlj4tWgyzLo+8F6SIPbW7zIYw=",
          "ip": "192.168.1.116",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEABK13LqOyxq7skjywUZwpTTLVXU3yPMSClL0u9xI5+hg=",
          "ip": "192.168.1.103",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x3292FEAbea61A76cf59Fa917b9DCcC937Ca489eE",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAz7Y+YE+zTAZO26NcyvbWFpwPOYS18kyofL9pitE73G0=",
          "ip": "192.168.1.117",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x372b320ECA35F86A28249E3e309545A44270DD7D",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAJJnp6slecl6UN0fjGiWya9a37N0iwUW1gQBS3Sh0qvU=",
          "ip": "192.168.1.101",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAr8qDQ8MYYxD26OVtzmLshwDH44rbtFcxp+n7YMsvit8=",
          "ip": "192.168.1.96",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x3CA9403151e5E7ad6072c9CF29237A3BB61eFaF3",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAl0V//ZTw/56RkIUtrEzyXIbPm0nQ+XjB2QEDZR+KbT4=",
          "ip": "192.168.1.98",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEANFAhkjOUKAp0RbqjjiDetKQjcwQTXLRpL0Vh7uz3Sm0=",
          "ip": "192.168.1.119",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x69b34b7538DeB6913f2b9f59Cbc8610059442e5A",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEApiP9nArs1ZDRXH3k89VuRReOlgNufYsF939nC3pBsqg=",
          "ip": "192.168.1.35",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x6a72ad3e9762d67D45a311954CdC6ad4693203a9",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAQjLIZj6+3TH2mSye+RS2HqN5W1+cGSg63ghfEOvBDnc=",
          "ip": "192.168.1.81",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAawp+8tDyeSREnNHrEaeBs6B9AeclJOlrAkeWMijTPww=",
          "ip": "192.168.1.114",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x855052fa258B463AEAd1E5abD55F2ffbCBb3F022",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAwigpWZg9E0DRbbbNuE4PDHT7MJ9XIH2hh5yADHNa6jw=",
          "ip": "192.168.1.89",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x8C33DF5ca4a4de15B53316dc3db60Ae4A7e09734",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEApakW/x/DvV7BBRmhbQzkxhj7xbS0Xr5JN4tSEigWshA=",
          "ip": "192.168.1.105",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x8F66e288547032026dd1ddFb992ff7eEcD9261f0",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAbA5Gq2olxI11gecRsyYYmaecJN0ht74mB2fLNWb3TcQ=",
          "ip": "192.168.1.115",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x8fFb06c288C30F3e62b31d6c5FD34328A964774a",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAner1iR+SqRLmN0lLWB0+su0Quh0XpNDTmm9PWWODirI=",
          "ip": "192.168.1.111",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x9234e37d86AE7De3Dd0Ac57AF815b54551873504",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAcUcydwF7CSr9bjBiUbd3drV+WMd4yd8xFL7HWGA4FTw=",
          "ip": "192.168.1.113",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x93E70Da36F35934C704ca9f2d2CF5cbc3Cba5988",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEARRkX0aksdpaxlbCExPkiaYaga6T/i2/iJyPGRTTNDm8=",
          "ip": "192.168.1.91",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xB6AE1C10C5547ed1D6ba50d74cc92214E17b5111",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAkHwtzRc4cHtDid6kE/hqO/h6bPlU+cG5ZigBEwOGD2Y=",
          "ip": "192.168.1.88",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xD82a5740De434f67b64946ba5939dfECc594Bcc1",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAB13mSe2XJ46JzM6WC3sOh7dh5TlMaDevNUlX7b4tuu8=",
          "ip": "192.168.1.109",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xE2EBF3781D7eFeCbf242a5510AAb60985E045F17",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAktscT7UBR2sjjapjsIjA00bR5vg3I62vPu1HcXQkzrM=",
          "ip": "192.168.1.108",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEA+X/pIfbC/gTA+iuG5yoLn6AH90PFdko5gWfURmCYC90=",
          "ip": "192.168.1.87",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAYc23TU7Tw6L9QcUXNM6FuS5kEzTTQEfX15dR9+n251Y=",
          "ip": "192.168.1.93",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAQ05ytVs7kiZxfN2f6PUT9XpjfASpuMxoDNTJkzmimew=",
          "ip": "192.168.1.90",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xc6C621E6BA9Ad2FA2E81998006e0f4Ff45c34b65",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEALUncL09pHgayYIMkZS+hbq5t61CIHG0juNkcbAo9abE=",
          "ip": "192.168.1.106",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xca3B60adeEf20337427b0d4Fa6E62920ea81a855",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAdTGsapuDIoqcgqXHYKJgNPuTkwhZ6EYGi9ORPXV7krQ=",
          "ip": "192.168.1.97",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xd56d950d5a79d7906269f87FEa9d1FE48Cb577E7",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAAXU9Om/NJRE0T7lo3L1b/QMcd6cBmGRW1/Y4jX2xiHQ=",
          "ip": "192.168.1.60",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAZVRP0epGewUhFeh7p6tvzX3Rhn4BSB/7Exjqr8hW5yk=",
          "ip": "192.168.1.110",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xdaAfa89eafe616EEa5Aa219d93bC8b1C0299Cc9E",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEAbrU2gaKp26A8Tmn7S0bMTTBJ5BrnLCv450l6oU+ixZM=",
          "ip": "192.168.1.107",
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0x5c8bf650F93d82A7131C2FeA01Ec2bFB3C61A03B",
          "height": "590",
          "identity": "MCowBQYDK2VwAyEASFAPKN8n+Nqn2RcJX8XCgyx1sveBLZ/f5tn5JpM2Xxs=",
          "ip": "123.121.14.187",
          "version": "1_1.0.0_d"
        }
      ],
      "message": "success",
      "version": "1_1.0.0_d"
    },
    "message": "success"
  }
}
```

### GetBonusInfo

Obtain node signature information

**Argument**

- None

**Returned value**

- code
  - 0 success
  - -1 DB get sign addr failed!
- message
- address Node address
- count Number of signatures
- time  Time spent

```json
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{}
}
```

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBonusInfo",
  "result": {
    "code": 0,
    "info": {
      "addr_count": [
        {
          "address": "0xCA66A76E2a279050EF6b57797ac53199379abB9F",
          "count": 3
        },
        {
          "address": "0xdaAfa89eafe616EEa5Aa219d93bC8b1C0299Cc9E",
          "count": 4
        },
        {
          "address": "0x5c8bf650F93d82A7131C2FeA01Ec2bFB3C61A03B",
          "count": 4
        },
        {
          "address": "0xca3B60adeEf20337427b0d4Fa6E62920ea81a855",
          "count": 2
        },
        {
          "address": "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce",
          "count": 3
        },
        {
          "address": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f",
          "count": 4
        },
        {
          "address": "0x8C33DF5ca4a4de15B53316dc3db60Ae4A7e09734",
          "count": 3
        },
        {
          "address": "0x116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2",
          "count": 4
        },
        {
          "address": "0x3812aE1f4a85A937340e882e4285f2CdaaCbC21F",
          "count": 2
        },
        {
          "address": "0x3CA9403151e5E7ad6072c9CF29237A3BB61eFaF3",
          "count": 3
        },
        {
          "address": "0x855052fa258B463AEAd1E5abD55F2ffbCBb3F022",
          "count": 5
        },
        {
          "address": "0x01921896D8AAC12B19BC8413135907AB5aE82326",
          "count": 5
        },
        {
          "address": "0xd57730E2CE30d412cea04689C9cDE2f0846df169",
          "count": 13
        },
        {
          "address": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b",
          "count": 4
        },
        {
          "address": "0xbBE3F8cf409A4554AC4dC3307B0198967E68258F",
          "count": 8
        },
        {
          "address": "0x93E70Da36F35934C704ca9f2d2CF5cbc3Cba5988",
          "count": 6
        },
        {
          "address": "0x28bA6E30cB0d9372a18c80552eE11DFe47883FAd",
          "count": 1
        },
        {
          "address": "0xFFFc74b51BC5e75527fE5970D04355958dd3657C",
          "count": 10
        },
        {
          "address": "0xB6AE1C10C5547ed1D6ba50d74cc92214E17b5111",
          "count": 10
        },
        {
          "address": "0x3292FEAbea61A76cf59Fa917b9DCcC937Ca489eE",
          "count": 8
        },
        {
          "address": "0x9234e37d86AE7De3Dd0Ac57AF815b54551873504",
          "count": 6
        },
        {
          "address": "0x372b320ECA35F86A28249E3e309545A44270DD7D",
          "count": 9
        },
        {
          "address": "0x79c80a68Cc851d9A2aBF16c32eBAaC866C4Fced9",
          "count": 5
        },
        {
          "address": "0x8fFb06c288C30F3e62b31d6c5FD34328A964774a",
          "count": 7
        },
        {
          "address": "0xc6C621E6BA9Ad2FA2E81998006e0f4Ff45c34b65",
          "count": 15
        },
        {
          "address": "0xE2EBF3781D7eFeCbf242a5510AAb60985E045F17",
          "count": 3
        },
        {
          "address": "0x3b5AF36c2F269c4eA5ADffd12d65818A9cd94Dc2",
          "count": 6
        },
        {
          "address": "0x244125ddD7A63479F3A5DA8bC36682EdaFfdc92d",
          "count": 5
        },
        {
          "address": "0x8F66e288547032026dd1ddFb992ff7eEcD9261f0",
          "count": 7
        },
        {
          "address": "0x2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5",
          "count": 5
        },
        {
          "address": "0xD82a5740De434f67b64946ba5939dfECc594Bcc1",
          "count": 10
        },
        {
          "address": "0x0a887Ad7a0a383e8fF9E1CB2433712e53C26AF95",
          "count": 2
        }
      ],
      "time": "1717113600000000"
    },
    "message": "message"
  }
}
```

### GetStakeUtxo

Get the pledged utxo

**Argument**

- fromaddr address

**Returned value**

- code
  - 0 success
  - -1 fromaddr not stake!

- message Return information (see code corresponding error return information for details)
- utxo utxo at the time of pledge
- value The amount at the time of pledge

```json
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{"fromAddr":"5c8bf650F93d82A7131C2FeA01Ec2bFB3C61A03B"}
}
```

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetAllStakeNodeList",
  "result": {
    "code": 0,
    "message": "",
    "utxos": {
      "827022b125d2b60e9ed40a1e7bfa6874b90bb6dbccd515824cb353f0ab3397c6": 100000000000
    }
  }
}
```

### GetDisinvestUtxo

Get the uninvested utxo

**Argument**

- fromAddr Investor
- toAddr investee

Returned value

- code
  - 0 success 
  - -1 The address has no investment in anyone
- message
- utxos  Uninvest utxo

```json
{
  "id":"1",
  "jsonrpc":"2.0",
  "params":{
    "fromAddr":"5c8bf650F93d82A7131C2FeA01Ec2bFB3C61A03B",
    "toAddr":"5c8bf650F93d82A7131C2FeA01Ec2bFB3C61A03B"
  }
}
```

```json
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetAllStakeNodeList",
  "result": {
    "code": 0,
    "message": "success",
    "utxos": {
      "utxo": [
        "17c62bacc4db9eee7a9b4596894dbf6a17754319fc8b24204fd4e7519a3f4457"
      ]
    }
  }
}
```



### GetBalance

**Instructions**:

Returns the account balance for the given address

**Argument**:

* id Transparent information

* jsonrpc  json version

* params argument

  * addr Address to query
  
  ​	

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    0  	sucess
    -1   address is invalid
    -2   search balance failed
  * message Call information
  * balance Account balance
  * addr The address to query


**Examples**:

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
    "params":{"addr":"0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBalance",
  "result": {
    "addr": "0x0796B6DB27e5eb1e9F8Bd2c4d03191C902D22F0f",
    "balance": "1905999939500",
    "code": 0,
    "message": "success"
  }
}
```



### GetBlockNumber

**Instructions**:

Returns the number of the latest block

**Argument**:

* id Transparent information
* jsonrpc  json version
**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    -  0  	sucess
    -  -1   GetBlockTop error
  * message Call information
  * top The number of the latest block

**Example**:

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBlockNumber",
  "result": {
    "code": 0,
    "message": "success",
    "top": "590"
  }
}
```



### GetVersion

**Instructions**:

Returns the current client version, network version, database version, and config version

**Argument**:

* id Transparent information
* jsonrpc  json version

**Returned value**:

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    -  0  	sucess
  * message Call information
  * clientVersion Client version
  * netVersion   Network version
  * configVersion   config version
  * dbVersion  Database version

**Example**:

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetVersion",
  "result": {
    "clientVersion": "1_1.0.0_d",
    "code": 0,
    "configVersion": "1.0.0",
    "dbVersion": "1_1.0.0_d",
    "message": "success",
    "netVersion": "1"
  }
}
```



### GetBlockTransactionCountByHash

**Instructions**:

Returns the number of transactions in a block that matches the hash of a given block

**Argument**:

* id Transparent information
* jsonrpc  json version
* params Argument
  * blockHash Block hash

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    *  0  	sucess
    *  -1   GetBlockByBlockHash error
    *  -2   block parse string fail
  * message Call information
  * txCount The number of transactions in the block for a given block hash

**Example**:

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
    "params":{"blockHash":"0x12e52383dc0fedc40bdab13fc1afd851d7123facf030f90163c03f87411650f1"}
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetBlockTransactionCountByHash",
  "result": {
    "code": 0,
    "message": "success",
    "txCount": "1"
  }
}
```







### GetAccounts

**Instructions**:

Returns a list of addresses owned by the client

**Argument**:

* id Transparent information
* jsonrpc  json version

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    - 0  	sucess
  * message Call information
  * acccountlist List of addresses owned by the client

**Example**: 

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetAccounts",
  "result": {
    "acccountlist": [
      "0x6a72ad3e9762d67D45a311954CdC6ad4693203a9",
      "0x87dE53fdC1e5AA53eB9Cb839C2EF664Cab0f4C01",
      "0x9d394DFB4475Eaef15A27396568e5028f13C3F85",
      "0xD4c60A4866BeE49e0642feC293ee8560C237b758",
      "0xf535227CCA5487776e666374c839de8b7005892B"
    ],
    "code": 0,
    "message": "success"
  }
}
```



### GetChainId

**Instructions**:

Return chain ID

**Argument**:

* id Transparent information

* jsonrpc  json version

  

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    -  0  	sucess
  * message Call information
  * chainId Chain ID

**Example**:

```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetChainId",
  "result": {
    "chainId": "0x1080c0ce",
    "code": 0,
    "message": "success"
  }
}
```



### GetPeerList

**Instructions**:

Returns the list of nodes currently connected to the client

**Argument**:

* id Transparent information

* jsonrpc  json version

  

**Returned value**:

* id Transparent information
* jsonrpc  json version
* method Method name
* result Return information
  * code Returned value
    -  0  	sucess
  * message Call information
  * peers  List of nodes connected to the client
  * size Number of nodes connected to the client



```json
//req
{
    "id":"1",
    "jsonrpc":"2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetPeerList",
  "result": {
    "code": 0,
    "message": "success",
    "peers": [
      {
        "addr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b", //Account address
        "fd": 16,  		//File descriptor.
       "pulse": "3",		//Heartbeat
        "height": 2499,  	//Current height of node
        "ip": "192.168.1.100", 	//Remote ip
        "ip_l": "192.168.1.81", 	//Own ip
        "kind": 1,    		// Connection type
        "name": "",    		//Node name
        "logo": "",   		//Browser flag
        "port": 55302, 		//Local port number
        "port_l": 20619, 	//Remote port number
        "version": "1_1.0.0_d" 	//Client version
      },
      {
        "addr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169",
        "fd": 17,
        "pulse": 3,
        "height": 2499,
        "ip": "192.168.1.110",
        "ip_l": "192.168.1.81",
        "kind": 1,
        "name": "",
         "logo": "",
        "port": 36874,
        "port_l": 20619,
        "version": "1_1.0.0_d"
      }
    ],
    "size": 2
  }
}
```

### GetRatesInfo

Get interest rate information

**Argument**:None

**Returned value**

- code Return value number
  - -101:Failed to get the current highest block height
  - -102:Failed to claim Utxo via periodic fetch
  - -103:Failure to retrieve transaction via hash
  - -104:Deserialization transaction failed
  - -201:Failed to obtain the total burn amount
  - -202:Failed to get the burn amount through the cycle
  - -203:The amount destroyed on the day was greater than the total amount destroyed
  - -301:Failure to obtain the total investment amount
  - -302:Obtaining investment utxo through the cycle fails
  - -303:Failure to retrieve transaction via hash
  - -304:Deserialization transaction failed
  - -1:The earning Rate is greater than the threshold
- TotalCirculatingSupply General circulation
- TotalBurn Total destruction
- TotalStaked Gross pledge
- StakingRate Pledge rate
- CurrentAPR Annualized rate

Example:

```json
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
}
//ack
{
  "id": "1",
  "jsonrpc": "2.0",
  "method": "GetPeerList",
  "result": {
    "code": 0,
    "message": "success",
    "peerList": {
      "listNodes": [
        {
          "addr": "0x0aFeBC02da4d5111d05d425e74e822B032274f2b",
          "fd": 16,
          "heartProbes": 3,
          "height": 2491,
          "ip": "192.168.1.100",
          "ip_l": "192.168.1.81",
          "kind": 1,
          "name": "",
          "port": 54432,
          "port_l": 20619,
          "version": "1_1.0.0_d"
        },
        {
          "addr": "0xd57730E2CE30d412cea04689C9cDE2f0846df169",
          "fd": 17,
          "heartProbes": 3,
          "height": 2491,
          "ip": "192.168.1.110",
          "ip_l": "192.168.1.81",
          "kind": 1,
          "name": "",
          "port": 36004,
          "port_l": 20619,
          "version": "1_1.0.0_d"
        }
      ],
      "peernodeSize": 2
    }
  }
}
```

### GetDelegateInfo

**Instructions**:

Obtain the invested information of the address according to the address. The maximum amount that can be invested in an address is: 65000 * 100000000

**Argument**:

* id Transparent information
* jsonrpc  json version
* params Argument
  * addr The address to query

**Returned value**:

* id Transparent information

* jsonrpc  json version

* method Method name

* result Return information

  * code Returned value
    * 0	success
    * -1   Database abnormal, Get invest addrs by node failed!
  * -2   The account number to be invested have been invested by 999 people
    * -3   Database abnormal, Get bonus addr invest utxos by bonusAddr failed
    * -4   Database abnormal, Get transaction by hash failed
    * -5   Failed to parse transaction body
  * message Call information
  * info  Investment address and investment amount
  
  ```json
  //req
  {
    "id":"1",
    "jsonrpc":"2.0",
    "params":{"addr":"0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce"}
  }
  //ack
  {
    "id": "1",
    "jsonrpc": "2.0",
    "method": "GetDelegateInfo",
    "result": {
      "code": 0,
      "info": {
        "0x3389E3e87EFC0464df70C8be58656274A66252af": "500000000000",
        "0x50fa281932a411e323dA8EA59269101DdF81C96C": "600000000000",
        "0x638c172F63db3caf32c410D0188143E0Eff74bC8": "800000000000",
        "0xadc2A709EC1413eCcEB4d115E50BD9ebBA35E3Ce": "1000000000000"
      },
      "message": "success"
    }
  }
  ```
  

## Transaction correlation

The process of sending transactions from the current account is as follows:

1. Determine the time difference between this transaction and the previous transaction sent on this account. On the APP side, after calling the two interfaces that send transactions, the content returned by the two interfaces is parsed, and the transaction information is cached locally. The confirmation interface (ConfirmTransaction) return txJson structure contains the information such as time and gas trading, and call interface (GetcallContractTransaction) contract request return of txJson also contains the information such as transaction time and gas. Also, the interface that sends a message (SendMessage) or a contract message (SendContractMessage) returns a txhash.

2. Check whether code in result is 0 to check whether the interface is called properly. The next interface call can be made only if the interface call code is 0.

3. All transaction interfaces adopt Post request mode, and the data format in the request body is JSON.

* Within 30 seconds of the time difference, it is necessary to judge whether the last transaction has been successfully connected, and the current transaction will be sent if it is successfully connected. If it is not successfully connected, the user will be prompted to operate frequently.
* Time difference greater than or equal to 30 seconds, directly send this transaction.

Determine whether the transaction was successfully connected

1. Obtain the node height and call the GetBlockNumber interface to obtain the node height as the value of the top field in the result
2. Call the ConfirmTransaction interface and pass the height field value to the top field returned by the GetBlockNumber interface. Txhash transmits the txhash value returned by the SendMessage or SendContractMessage interface for the last transaction sent by the current account. If the percent field returned by the ConfirmTransaction interface is greater than or equal to 0.8, the transaction is successfully connected.

## Send tfs transactions

First, the transaction interface such as GetTransaction is called, and then all the contents returned by the GetTransaction interface are signed by calling the Sig method in the library. Then the /SendMessage interface is called. The request parameter of the /SendMessage interface is the JSON string returned by the sigTx method.

### SendMessage

**Instructions**:

For GetTransaction, GetStakeTransaction, GetUnStakeTransaction, GetInvestTransaction, GetDisInvestTransaction, GetBouns and other interfaces, After the call is completed, the signature SDK tool is used to sign the transaction and the SendMessage interface is used to send the transaction to the node. The ConfirmTransaction interface is used to determine whether to link.

**Argument**:

Call the return value of the SDK tool signature interface for the data returned by an interface such as GetTransaction

**Returned value**:

No returned value, after invoking this interface, check whether the link is connected

**Example**:

```json
// The data returned by GetTransaction is signed
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

### SendContractMessage

**Instructions**:

// The data returned by GetTransaction is signed

**Argument**:

For GetDeployContractTransaction interface data returned by the call SDK tools such as the return value of the signature interface

**Returned value**:

No returned value, call this interface to see if the chain is on

**Example**:

```json
//req
{
    "id": "",
    "jsonrpc": "",
    "result": {
        "code": "",
        "contractJs": "{\"version\":\"1_1.0.0_d\",\"txMsgReq\":{\"version\":\"1_1.0.0_d\",\"txMsgInfo\":{\"nodeHeight\":\"601\",\"contractStorageList\":[\"A8B8Ae6F84709fF80E08aD9d26575c161aCC95f1\"]},\"vrfInfo\":{\"vrfdata\":{\"hash\":\"dea1b44a641928d6a09db9a3d9da274abe4ef13eb23833213144a5b46c612136\"},\"Vrfsign\":{\"pub\":\"MCowBQYDK2VwAyEASFAPKN8n+Nqn2RcJX8XCgyx1sveBLZ/f5tn5JpM2Xxs=\"}}}}",
        "message": "",
        "txJson": "{\"time\":\"1717148103333839\",\"identity\":\"2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"dea1b44a641928d6a09db9a3d9da274abe4ef13eb23833213144a5b46c612136\"}],\"vinSign\":{\"sign\":\"3o82Rq7taGO+VRtrhtxWOVPAolo/pVxuNXEBdklDpDVd8tJcTjNrnmaMFixdav2wCyvCb+AFOd02ryPI4JV1Cw==\",\"pub\":\"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=\"}}],\"vout\":[{\"value\":\"480\",\"addr\":\"VirtualDeployContractBurnGas\"},{\"value\":\"1982446498797\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"493200\",\"addr\":\"VirtualBurnGas\"}],\"multiSign\":[{\"sign\":\"YVcOA5gZhVNaQx7eoduw4lOI4d1HNtPRWEUoMzDK6D2UnZXDbRziXV66XiaRxKOzXF3kF/N4j8PEe5CMjkf3BQ==\",\"pub\":\"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":7,\"data\":\"{\\\"TxInfo\\\":{\\\"blockPrevRandao\\\":4406,\\\"blockTimestamp\\\":1717148110,\\\"input\\\":\\\"608060405234801561001057600080fd5b506108b3806100206000396000f3fe608060405234801561001057600080fd5b50600436106100575760003560e01c80630483a7f61461005c5780631629614e1461008c57806327e235e3146100a85780637ad9ad7c146100d8578063afc58189146100f4575b600080fd5b610076600480360381019061007191906105a8565b610110565b60405161008391906106d7565b60405180910390f35b6100a660048036038101906100a19190610615565b610128565b005b6100c260048036038101906100bd91906105a8565b6102a7565b6040516100cf91906106d7565b60405180910390f35b6100f260048036038101906100ed91906105d5565b6102bf565b005b61010e60048036038101906101099190610615565b61037d565b005b60016020528060005260406000206000915090505481565b80806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000205410156101aa576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016101a1906106b7565b60405180910390fd5b816000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546101f89190610759565b9250508190555081600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461024e9190610703565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f3a14c6aa3e15c61c97825b026647b989a91e18aa33b689769475a298922480428360405161029b91906106d7565b60405180910390a25050565b60006020528060005260406000206000915090505481565b806000808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461030d9190610703565b925050819055508173ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff167f322d0c4befd4c2dd440740b711488a1638fd7d8eeb25f9dacede84083db428c98360405161037191906106d7565b60405180910390a35050565b6000600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541415610400576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016103f790610697565b60405180910390fd5b80600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541015610482576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161047990610697565b60405180910390fd5b806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546104d09190610703565b9250508190555080600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546105269190610759565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f867b353f032680758428983522443995b88120a470e436b962c6a9d0d8940af78260405161057391906106d7565b60405180910390a250565b60008135905061058d8161084f565b92915050565b6000813590506105a281610866565b92915050565b6000602082840312156105be576105bd6107f8565b5b60006105cc8482850161057e565b91505092915050565b600080604083850312156105ec576105eb6107f8565b5b60006105fa8582860161057e565b925050602061060b85828601610593565b9150509250929050565b60006020828403121561062b5761062a6107f8565b5b600061063984828501610593565b91505092915050565b600061064f6011836106f2565b915061065a826107fd565b602082019050919050565b60006106726014836106f2565b915061067d82610826565b602082019050919050565b610691816107bf565b82525050565b600060208201905081810360008301526106b081610642565b9050919050565b600060208201905081810360008301526106d081610665565b9050919050565b60006020820190506106ec6000830184610688565b92915050565b600082825260208201905092915050565b600061070e826107bf565b9150610719836107bf565b9250827fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff0382111561074e5761074d6107c9565b5b828201905092915050565b6000610764826107bf565b915061076f836107bf565b925082821015610782576107816107c9565b5b828203905092915050565b60006107988261079f565b9050919050565b600073ffffffffffffffffffffffffffffffffffffffff82169050919050565b6000819050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b600080fd5b7f4e6f206c6f636b65642062616c616e6365000000000000000000000000000000600082015250565b7f496e73756666696369656e742062616c616e6365000000000000000000000000600082015250565b6108588161078d565b811461086357600080fd5b50565b61086f816107bf565b811461087a57600080fd5b5056fea264697066735822122067e67aed3152cf78a07c4f8842540cf5803e421699b10fbf8f66c015550b0ed464736f6c63430008070033\\\",\\\"recipient\\\":\\\"A8B8Ae6F84709fF80E08aD9d26575c161aCC95f1\\\",\\\"sender\\\":\\\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\\\",\\\"version\\\":0,\\\"virtualMachine\\\":0}}\"}"
    }
}
```

### GetTransaction

Get the general transaction body

**Argument**

- fromAddr Initiator address
- toAddr Receiving address
- isFindUtxo Whether to search the current utxo status across the network
- value Transfer amount
- txDescriptionInfo: Transaction description information

**Returned value**

- code Return value number
  - 0     success
  - -1    db get top failed
  - -2    Check parameters failed
  - -3     to addr is empty
  - -4     To address is not  address!
  - -5     from address is same with toaddr
  - -6     Value is zero!
  - -7     The information entered exceeds the specified length
  - -8     FindUtxo failed!
  - -9     Utxo is empty!
  - -10    Tx owner is empty!
  - -11     Generate Gas failed!
  - -12     Insufficient balance (formerly -72013)
  - -13     Find packager failed
  - -14     utxo is using!

- message Return value information (see code for error return information)
- txJson:  Transaction body information
- height:  Chain height
- vrfJson: Vrf information
- txType:  Type of transaction
- time:    The time the transaction was sent
- gas:     gas cost

```json
{"id":"","jsonrpc":"","params":{"fromAddr":["cED97dA085527Fe7e1772CA59Aa1e64A78143128"],"isFindUtxo":false,"toAddr":[{"addr":"06BA76F46631d4F344d1344303895001F1E3Af29","value":"13.5"}],"txInfo":""}}
```

```json
{"id":"","jsonrpc":"","method":"","result":{"code":0,"gas":"20200","height":"600","message":"0","time":"1717148047269517","txJson":"{\"time\":\"1717148047269517\",\"identity\":\"2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"3f1342e96e426e2905021ad991787131ec70d31298646b1e80da9d912eeff274\"}]}],\"vout\":[{\"value\":\"1350000000\",\"addr\":\"06BA76F46631d4F344d1344303895001F1E3Af29\"},{\"value\":\"1982446992477\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"20200\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":1}","txType":"1","vrfJson":"{\"vrfdata\":{\"hash\":\"6cf89d80c98eecd9138caca4f55d7ad0fda2aed9d8e68dd4642543ae3ee056d6\"},\"Vrfsign\":{\"sign\":\"u5dNZ16Rd77B4nLd8gAcKTwz+GxeHH1HIlcGennGbPaKgIFXUkmFzS/EnVxRC4nmSfESAdWyMEmj4pKBhwuqAg==\",\"pub\":\"MCowBQYDK2VwAyEAcUcydwF7CSr9bjBiUbd3drV+WMd4yd8xFL7HWGA4FTw=\"}}"}}
```

### GetDeployContractTransaction

Get a deployment contract transaction

**Argument**

- addr Deployment address
- contract Contract deployment code
- nContractType By default 0
- info Contract information
- data Contract code
- pubstr Base64 of the deployment address public key
- isFindUtxo Whether to search the current utxo status across the network
- txDescriptionInfo: Transaction description information

**Returned value**

- code Return value number
  - 0 success
  - -300 Failure of the execution contract (whether the output error information is not fixed)
  - -2004 The main network currency balance is insufficient
  - -13114 The main network currency balance is insufficient
  - -13116 reward less than gas
  - -13117 The main network currency balance is insufficient


- message Return value information((For details, see the code corresponding error return information))
- contractJs Contract information
- txJson Transaction information

```json
{"id":"","jsonrpc":"","params":{"addr":"cED97dA085527Fe7e1772CA59Aa1e64A78143128","contract":"608060405234801561001057600080fd5b506108b3806100206000396000f3fe608060405234801561001057600080fd5b50600436106100575760003560e01c80630483a7f61461005c5780631629614e1461008c57806327e235e3146100a85780637ad9ad7c146100d8578063afc58189146100f4575b600080fd5b610076600480360381019061007191906105a8565b610110565b60405161008391906106d7565b60405180910390f35b6100a660048036038101906100a19190610615565b610128565b005b6100c260048036038101906100bd91906105a8565b6102a7565b6040516100cf91906106d7565b60405180910390f35b6100f260048036038101906100ed91906105d5565b6102bf565b005b61010e60048036038101906101099190610615565b61037d565b005b60016020528060005260406000206000915090505481565b80806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000205410156101aa576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016101a1906106b7565b60405180910390fd5b816000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546101f89190610759565b9250508190555081600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461024e9190610703565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f3a14c6aa3e15c61c97825b026647b989a91e18aa33b689769475a298922480428360405161029b91906106d7565b60405180910390a25050565b60006020528060005260406000206000915090505481565b806000808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461030d9190610703565b925050819055508173ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff167f322d0c4befd4c2dd440740b711488a1638fd7d8eeb25f9dacede84083db428c98360405161037191906106d7565b60405180910390a35050565b6000600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541415610400576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016103f790610697565b60405180910390fd5b80600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541015610482576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161047990610697565b60405180910390fd5b806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546104d09190610703565b9250508190555080600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546105269190610759565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f867b353f032680758428983522443995b88120a470e436b962c6a9d0d8940af78260405161057391906106d7565b60405180910390a250565b60008135905061058d8161084f565b92915050565b6000813590506105a281610866565b92915050565b6000602082840312156105be576105bd6107f8565b5b60006105cc8482850161057e565b91505092915050565b600080604083850312156105ec576105eb6107f8565b5b60006105fa8582860161057e565b925050602061060b85828601610593565b9150509250929050565b60006020828403121561062b5761062a6107f8565b5b600061063984828501610593565b91505092915050565b600061064f6011836106f2565b915061065a826107fd565b602082019050919050565b60006106726014836106f2565b915061067d82610826565b602082019050919050565b610691816107bf565b82525050565b600060208201905081810360008301526106b081610642565b9050919050565b600060208201905081810360008301526106d081610665565b9050919050565b60006020820190506106ec6000830184610688565b92915050565b600082825260208201905092915050565b600061070e826107bf565b9150610719836107bf565b9250827fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff0382111561074e5761074d6107c9565b5b828201905092915050565b6000610764826107bf565b915061076f836107bf565b925082821015610782576107816107c9565b5b828203905092915050565b60006107988261079f565b9050919050565b600073ffffffffffffffffffffffffffffffffffffffff82169050919050565b6000819050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b600080fd5b7f4e6f206c6f636b65642062616c616e6365000000000000000000000000000000600082015250565b7f496e73756666696369656e742062616c616e6365000000000000000000000000600082015250565b6108588161078d565b811461086357600080fd5b50565b61086f816107bf565b811461087a57600080fd5b5056fea264697066735822122067e67aed3152cf78a07c4f8842540cf5803e421699b10fbf8f66c015550b0ed464736f6c63430008070033","data":"","info":"[]","isFindUtxo":false,"nContractType":"0","pubstr":"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=","txInfo":"info"}}
```

```json
{"id":"","jsonrpc":"","method":"","result":{"code":0,"contractJs":"{\"version\":\"1_1.0.0_d\",\"txMsgReq\":{\"version\":\"1_1.0.0_d\",\"txMsgInfo\":{\"nodeHeight\":\"601\",\"contractStorageList\":[\"A8B8Ae6F84709fF80E08aD9d26575c161aCC95f1\"]},\"vrfInfo\":{\"vrfdata\":{\"hash\":\"dea1b44a641928d6a09db9a3d9da274abe4ef13eb23833213144a5b46c612136\"},\"Vrfsign\":{\"pub\":\"MCowBQYDK2VwAyEASFAPKN8n+Nqn2RcJX8XCgyx1sveBLZ/f5tn5JpM2Xxs=\"}}}}","message":"","txJson":"{\"time\":\"1717148103333839\",\"identity\":\"2eb2F635320c3Dbf29eadD35E894c13EE3F20bd5\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"dea1b44a641928d6a09db9a3d9da274abe4ef13eb23833213144a5b46c612136\"}]}],\"vout\":[{\"value\":\"480\",\"addr\":\"VirtualDeployContractBurnGas\"},{\"value\":\"1982446498797\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"493200\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":7,\"data\":\"{\\\"TxInfo\\\":{\\\"blockPrevRandao\\\":4406,\\\"blockTimestamp\\\":1717148110,\\\"input\\\":\\\"608060405234801561001057600080fd5b506108b3806100206000396000f3fe608060405234801561001057600080fd5b50600436106100575760003560e01c80630483a7f61461005c5780631629614e1461008c57806327e235e3146100a85780637ad9ad7c146100d8578063afc58189146100f4575b600080fd5b610076600480360381019061007191906105a8565b610110565b60405161008391906106d7565b60405180910390f35b6100a660048036038101906100a19190610615565b610128565b005b6100c260048036038101906100bd91906105a8565b6102a7565b6040516100cf91906106d7565b60405180910390f35b6100f260048036038101906100ed91906105d5565b6102bf565b005b61010e60048036038101906101099190610615565b61037d565b005b60016020528060005260406000206000915090505481565b80806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000205410156101aa576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016101a1906106b7565b60405180910390fd5b816000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546101f89190610759565b9250508190555081600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461024e9190610703565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f3a14c6aa3e15c61c97825b026647b989a91e18aa33b689769475a298922480428360405161029b91906106d7565b60405180910390a25050565b60006020528060005260406000206000915090505481565b806000808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020600082825461030d9190610703565b925050819055508173ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff167f322d0c4befd4c2dd440740b711488a1638fd7d8eeb25f9dacede84083db428c98360405161037191906106d7565b60405180910390a35050565b6000600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541415610400576040517f08c379a00000000000000000000000000000000000000000000000000000000081526004016103f790610697565b60405180910390fd5b80600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541015610482576040517f08c379a000000000000000000000000000000000000000000000000000000000815260040161047990610697565b60405180910390fd5b806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546104d09190610703565b9250508190555080600160003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282546105269190610759565b925050819055503373ffffffffffffffffffffffffffffffffffffffff167f867b353f032680758428983522443995b88120a470e436b962c6a9d0d8940af78260405161057391906106d7565b60405180910390a250565b60008135905061058d8161084f565b92915050565b6000813590506105a281610866565b92915050565b6000602082840312156105be576105bd6107f8565b5b60006105cc8482850161057e565b91505092915050565b600080604083850312156105ec576105eb6107f8565b5b60006105fa8582860161057e565b925050602061060b85828601610593565b9150509250929050565b60006020828403121561062b5761062a6107f8565b5b600061063984828501610593565b91505092915050565b600061064f6011836106f2565b915061065a826107fd565b602082019050919050565b60006106726014836106f2565b915061067d82610826565b602082019050919050565b610691816107bf565b82525050565b600060208201905081810360008301526106b081610642565b9050919050565b600060208201905081810360008301526106d081610665565b9050919050565b60006020820190506106ec6000830184610688565b92915050565b600082825260208201905092915050565b600061070e826107bf565b9150610719836107bf565b9250827fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff0382111561074e5761074d6107c9565b5b828201905092915050565b6000610764826107bf565b915061076f836107bf565b925082821015610782576107816107c9565b5b828203905092915050565b60006107988261079f565b9050919050565b600073ffffffffffffffffffffffffffffffffffffffff82169050919050565b6000819050919050565b7f4e487b7100000000000000000000000000000000000000000000000000000000600052601160045260246000fd5b600080fd5b7f4e6f206c6f636b65642062616c616e6365000000000000000000000000000000600082015250565b7f496e73756666696369656e742062616c616e6365000000000000000000000000600082015250565b6108588161078d565b811461086357600080fd5b50565b61086f816107bf565b811461087a57600080fd5b5056fea264697066735822122067e67aed3152cf78a07c4f8842540cf5803e421699b10fbf8f66c015550b0ed464736f6c63430008070033\\\",\\\"recipient\\\":\\\"A8B8Ae6F84709fF80E08aD9d26575c161aCC95f1\\\",\\\"sender\\\":\\\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\\\",\\\"version\\\":0,\\\"virtualMachine\\\":0}}\"}"}}
```

### GetCallContractTransaction

Get an execution contract transaction

**Argument**

- addr Executive address
- args Execution of contract parameters
- contractAddress Contract address
- deployer Deploy the contract address
- deployutxo Txhash for the deployment contract
- istochain Whether it's on the chain
- pubstr Base64 of the executor's public key
- tip  Cost tip
- info Information
- money Amount

**Returned value**

- code Return value number
  - 0 success
  - -300 Failure of execution contract(Judging whether the balance is insufficient according to the output error message)
  - -2004 The main network currency balance is insufficient
  - -13114 The main network currency balance is insufficient
  - -13116 reward less than gas
  - -13117 The main network currency balance is insufficient

- message Return value information((For details, see the code corresponding error return information),Omit the contents internal errors)
- contractJs Contract information
- txJson Transaction information

```json
{"id":"123","jsonrpc":"","params":{"addr":"cED97dA085527Fe7e1772CA59Aa1e64A78143128","args":"0x7ad9ad7c000000000000000000000000ff3778ca36a2936390c06d8b0457f5b8e408389c0000000000000000000000000000000000000000000000000000000000002710","contractAddress":"0x7350399179EC2B0702008aE8b43a0579AA699Eb1","deployer":"cED97dA085527Fe7e1772CA59Aa1e64A78143128","deployutxo":"0x8a02413da127b48318a7ed12a46a4f68b83cdc6c21f937d7e6c99393d64112b0","isFindUtxo":false,"istochain":"true","money":"0","pubstr":"MCowBQYDK2VwAyEA89VSBQU7d4uL+jvqAKeCRbgYz2tzk/Rf8DNRhB0sLbg=","tip":"0","txInfo":"info"}}
```

```json
{"id":"123","jsonrpc":"","method":"","result":{"code":0,"contractJs":"{\"version\":\"1_1.0.0_d\",\"txMsgReq\":{\"version\":\"1_1.0.0_d\",\"txMsgInfo\":{\"nodeHeight\":\"603\",\"contractStorageList\":[\"7350399179EC2B0702008aE8b43a0579AA699Eb1\"]},\"vrfInfo\":{\"vrfdata\":{\"hash\":\"79675c88de3a336d2e47c6134146f0a4d26e068ca76aa730ca654830c6bb6b96\"},\"Vrfsign\":{\"pub\":\"MCowBQYDK2VwAyEASFAPKN8n+Nqn2RcJX8XCgyx1sveBLZ/f5tn5JpM2Xxs=\"}}}}","message":"","txJson":"{\"time\":\"1717148359029088\",\"identity\":\"0aFeBC02da4d5111d05d425e74e822B032274f2b\",\"utxo\":{\"owner\":[\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"],\"vin\":[{\"prevOut\":[{\"hash\":\"79675c88de3a336d2e47c6134146f0a4d26e068ca76aa730ca654830c6bb6b96\"}]}],\"vout\":[{\"value\":\"25041\",\"addr\":\"VirtualCallContractBurnGas\"},{\"value\":\"1982446318715\",\"addr\":\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\"},{\"value\":\"65000\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":8,\"data\":\"{\\\"TxInfo\\\":{\\\"blockPrevRandao\\\":4345,\\\"blockTimestamp\\\":1717148360,\\\"contractDeployer\\\":\\\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\\\",\\\"donation\\\":0,\\\"input\\\":\\\"7ad9ad7c000000000000000000000000ff3778ca36a2936390c06d8b0457f5b8e408389c0000000000000000000000000000000000000000000000000000000000002710\\\",\\\"output\\\":\\\"\\\",\\\"recipient\\\":\\\"7350399179EC2B0702008aE8b43a0579AA699Eb1\\\",\\\"sender\\\":\\\"cED97dA085527Fe7e1772CA59Aa1e64A78143128\\\",\\\"transfer\\\":0,\\\"version\\\":0,\\\"virtualMachine\\\":0}}\"}"}}
```

### GetStakeTransaction

Obtain information on pledge transactions

**Argument**:

- fromAddr:Initiator address
- stakeAmount:Amount pledged
- PledgeType:Pledge type
- pumpingPercentage:Pledge pumping ratio
- isFindUtxo: Whether the current utxo state is detected
- txInfo: Transaction description information

**Returned value**:

- code Return value number
  - 0:success
  - -1:input pumping percentage error
  - -2:Failed to get the current highest block height
  - -3:Check parameters failed
  - -4:From address invlaid
  - -5:Stake amount is zero
  - -6:The pledge amount must be greater than Minimum pledge value
  - -7:Unknown stake type
  - -8:There has been a pledge transaction before !
  - -9:The information entered exceeds the specified length
  - -10:FindUtxo failed
  - -11:Utxo is empty
  - -12:Tx owner is invalid
  - -13:The commission ratio is not in the range
  - -14:The gas charge cannot be 0
  - -15:The total amount is less than gas
  - -16:Failed to get the packager
- message Return value information
- txJson: Transaction information
- height:Height
- vrfJson: vrf information
- txType:Transaction type
- time: The time the transaction was sent
- gas: Fuel cost



Example:

```json
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
    "params" : "{"fromAddr" : "69b34b7538DeB6913f2b9f59Cbc8610059442e5A", "stakeAmount" : "1000", "PledgeType" : "0","CommissionRate": "5", "isFindUtxo": true, "txInfo": ""}"
}

//ack
{"id":"1","jsonrpc":"2.0","method":"GetStakeTransaction","result":{"code":0,"gas":"28100","height":"593","message":"success","time":"1717146934713506","txJson":"{\"time\":\"1717146934713506\",\"identity\":\"8F66e288547032026dd1ddFb992ff7eEcD9261f0\",\"utxo\":{\"owner\":[\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"],\"vin\":[{\"prevOut\":[{\"hash\":\"1a9446933109a33766fde80ced93142b261f81e315bc8afd9abd5306239842c1\"}]}],\"vout\":[{\"value\":\"100000000000\",\"addr\":\"VirtualStake\"},{\"value\":\"1899899508900\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"28100\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":2,\"data\":\"{\\\"TxInfo\\\":{\\\"CommissionRate\\\":0.05,\\\"StakeAmount\\\":100000000000,\\\"StakeType\\\":\\\"Net\\\"}}\"}","txType":"0","vrfJson":"{}"}}



```



### GetUnStakeTransaction

Get a release transaction

**Argument**:

- fromAddr: Initiator address
- utxoHash:  Utxo hash
- isFindUtxo: Whether the current utxo state is detected
- txInfo: Transaction description information

**Returned value**:

- code Return value number
  
  - 0:success
  
  - -1:Failed to get the current highest block height
  - -2:Check parameters failed
  - -3: FromAddr is not normal addr.
  - -4:FindUtxo failed
  - -5:Utxo is empty
  - -6:Tx owner is empty
  - -7:The information entered exceeds the specified length
  - -8:The total amount is less than expend
  - -9:GetBlockPackager error
  - -101:Get all stake address failed
  - -102:The account number has not staked assets
  - -103:Get stake utxo from address failed
  - -104:The utxo to be de staked is not in the staked utxo
  - -105:The staked utxo is not more than 30 days
  - -106:Stake tx not found
  - -107:Failed to parse transaction body
  - -108:Stake value is zero
  
- message Return value information

- txJson: Transaction information

- height:Height

- vrfJson: vrf information

- txType:Transaction type

- time: The time the transaction was sent

- gas: Fuel cost

Example:

```json
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
    "params" : "{"fromAddr" : "69b34b7538DeB6913f2b9f59Cbc8610059442e5A", "utxoHash" : "405efe5ae260a8297751784ce5bb590efea1324b29c24b658b3b2e1ed948eec3","isFindUtxo": true, "txInfo": ""}"
}

//ack
{"id":"1","jsonrpc":"2.0","method":"GetUnStakeTransaction","result":{"code":0,"gas":"39300","height":"595","message":"success","time":"1717147041334522","txJson":"{\"time\":\"1717147041334522\",\"identity\":\"372b320ECA35F86A28249E3e309545A44270DD7D\",\"utxo\":{\"owner\":[\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\",\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"],\"vin\":[{\"prevOut\":[{\"hash\":\"b088fde1b1b270399134a7027408b2ef270d7f00859f306f9cb006e46de77e18\",\"n\":1}]},{\"prevOut\":[{\"hash\":\"e47b853d8d59e8d5982f68ed19dee6cdc5ce7e173df3e699af817366bd7b7541\"}],\"sequence\":1}],\"vout\":[{\"value\":\"100000000000\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"899899437600\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"39300\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":3,\"data\":\"{\\\"TxInfo\\\":{\\\"UnstakeUtxo\\\":\\\"b088fde1b1b270399134a7027408b2ef270d7f00859f306f9cb006e46de77e18\\\"}}\"}","txType":"0","vrfJson":"{}"}}
```

### GetInvestTransaction

Get investment trading information

**Argument**:

- fromAddr: Initiator address
- toAddr:  Invested address
- investAmount: Investment amount
- investType: Type of investment

- isFindUtxo: Whether the current utxo state is detected
- txInfo: Transaction description information

**Returned value**:

- code Return value number
  - 0:success
  
  - -1:Failed to get the current highest block height
  - -2:Check parameters failed
  - -3:The initiator address is incorrect
  - -4:The receiver address is incorrect
  - -5:investment amount less 35
  - -6:Unknown invest type
  - -7:The information entered exceeds the specified length
  - -8:FindUtxo failed
  - -9:Utxo is empty
  - -10:Tx owner is empty
  - -11:gas cannot be 0
  - -12:The total amount is less than expend
  - -13:GetBlockPackager error
  - -101:The investor have already invested in a node
  - -102:The investment amount is less than 35
  - -103:The account to be invested has not spent 500 to access the Internet
  - -104:Get invest addrs by node failed
  - -105:The account number to be invested have been invested by 999 people
  - -106:GetBonusAddrInvestUtxosByBonusAddr failed
  - -107:GetTransactionByHash failed
  - -108:Failed to parse transaction body
  - -109:The total amount invested in a single node will be more than 65000
  
- message Return value information

- txJson: Transaction information

- height:Height

- vrfJson: vrf information

- txType:Transaction type

- time: The time the transaction was sent

- gas: Fuel cost

Example:

```json
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
    "params" : "{"fromAddr" : "69b34b7538DeB6913f2b9f59Cbc8610059442e5A","toAddr":"69b34b7538DeB6913f2b9f59Cbc8610059442e5A","investAmount":"1000", "investType" : "0","pumpingPercentage": "5", "isFindUtxo": false, "txInfo": ""}"
}

//ack
{"id":"1","jsonrpc":"2.0","method":"GetInvestTransaction","result":{"code":0,"gas":"32000","height":"590","message":"success","time":"1717146585760939","txJson":"{\"time\":\"1717146585760939\",\"identity\":\"8fFb06c288C30F3e62b31d6c5FD34328A964774a\",\"utxo\":{\"owner\":[\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"],\"vin\":[{\"prevOut\":[{\"hash\":\"ed71842812bd3d5e0032d40f5a01ff8db1b0018a0a36c11292ed97e3783b2a78\"}]}],\"vout\":[{\"value\":\"1000000000000\",\"addr\":\"VirtualInvest\"},{\"value\":\"899899621300\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"32000\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":4,\"data\":\"{\\\"TxInfo\\\":{\\\"BonusAddr\\\":\\\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\\\",\\\"InvestAmount\\\":1000000000000,\\\"InvestType\\\":\\\"Normal\\\"}}\"}","txType":"0","vrfJson":"{}"}}

```



### GetDisInvestTransaction

Get the investment transaction information

**Argument**:

- fromAddr: Initiator address
- toAddr:  Invested address
- utxoHash: Invest in utxo hashing

- isFindUtxo: Whether the current utxo state is detected
- txInfo: Transaction description information

**Returned value**:

- code Return value number
  - 0:success
  
  - -1:Failed to get the current highest block height
  - -2:Check parameters failed 
  - -3:FromAddr is not normal addr.
  - -4:To address is not normal addr.
  - -5:The information entered exceeds the specified length
  - -6:FindUtxo failed
  - -7:Utxo is empty
  - -8:Tx owner is empty
  - -9:gas cannot be 0
  - -10:The total amount is less than expend
  - -11:GetBlockPackager error
  - -101:GetBonusAddrByInvestAddr failed
  - -102:The account has not invested assets to node
  - -103:GetBonusAddrInvestUtxosByBonusAddr failed
  - -104:The utxo to divest is not in the utxos that have been invested
  - -105:The invested utxo is not more than 1 day
  - -106:Invest tx not found
  - -107:Failed to parse transaction body
  - -108:The node to be divested is not invested
  - -109:The invested value is zero
  
- message Return value information

- txJson: Transaction information

- height:Height

- vrfJson: vrf information

- txType:Transaction type

- time: The time the transaction was sent

- gas: Fuel cost

```json
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
    "params" : "{"fromAddr" : "69b34b7538DeB6913f2b9f59Cbc8610059442e5A","toAddr":"69b34b7538DeB6913f2b9f59Cbc8610059442e5A","utxoHash":"db2caaf71ff57ec954e67cabede4a4b2207fd8645e684e66983eaefea63f4e2a","isFindUtxo": false, "txInfo": ""}"
}

//ack
{"id":"1","jsonrpc":"2.0","method":"GetDisInvestTransaction","result":{"code":0,"gas":"45000","height":"591","message":"success","time":"1717146744611408","txJson":"{\"time\":\"1717146744611408\",\"identity\":\"3292FEAbea61A76cf59Fa917b9DCcC937Ca489eE\",\"utxo\":{\"owner\":[\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\",\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"],\"vin\":[{\"prevOut\":[{\"hash\":\"3941c0cc427c3053222b9d1f32a2882a564e1ed3c45bcf59a48dc08c6eceb6e3\",\"n\":1}]},{\"prevOut\":[{\"hash\":\"3941c0cc427c3053222b9d1f32a2882a564e1ed3c45bcf59a48dc08c6eceb6e3\"}],\"sequence\":1}],\"vout\":[{\"value\":\"1000000000000\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"899899576300\",\"addr\":\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\"},{\"value\":\"45000\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":5,\"data\":\"{\\\"TxInfo\\\":{\\\"BonusAddr\\\":\\\"69b34b7538DeB6913f2b9f59Cbc8610059442e5A\\\",\\\"DisinvestUtxo\\\":\\\"3941c0cc427c3053222b9d1f32a2882a564e1ed3c45bcf59a48dc08c6eceb6e3\\\"}}\"}","txType":"0","vrfJson":"{}"}}

```



### GetBounsTransaction

Obtain the claim transaction information

**Argument**:

- Addr:  Claim address
- isFindUtxo:  Whether the current utxo state is detected
- txInfo:Transaction description information

**Returned value**:

- code Return value number
  
  - 0:success
  
  - -1:Failed to get the current highest block height
  - -2:Check parameters failed
  - -3:The bouns address is incorrect
  - -4:The information entered exceeds the specified length
  - -5:Failed to obtain the amount claimed by the investor
  - -6:FindUtxo failed
  - -7:utxo is zero
  - -8:Tx owner is empty!
  - -9:GetCommissionPercentage error
  - -10:The gas charge cannot be 0
  - -11:The total amount is less than expend
  - -12:The claim amount is 0
  - -13:GetBlockPackager fail
  - -101:The bouns time is not within the prescribed limits
  - -102:Incorrect time
  - -103:GetBonusUtxoByPeriod fail
  - -104:GetTransactionByHash fail
  - -105:Failed to parse transaction body
  - -106:GetBonusUtxoByPeriod fail
  - -107:VerifyBonusAddr fail
  - -108:The bouns address is not pledged
  
- message Return value information

- txJson: Transaction information

- height:Height

- vrfJson: vrf information

- txType:Transaction type

- time: The time the transaction was sent

- gas: Fuel cost

```json
//req
//req
{
    "id" : "1",
    "jsonrpc": "2.0",
    "params" : "{"Addr" : "116058AcF188BB96F9Da1317Bd11fD737E4f8Cd2","isFindUtxo": false, "txInfo": ""}"
}

//ack
{"id":"1","jsonrpc":"2.0","method":"GetBounsTransaction","result":{"code":0,"gas":"25600","height":"597","message":"success","time":"1717147601683173","txJson":"{\"time\":\"1717147601683173\",\"identity\":\"08C08F389c8255c0B4d1C5e337C811D02F220B6e\",\"utxo\":{\"owner\":[\"9234e37d86AE7De3Dd0Ac57AF815b54551873504\"],\"vin\":[{\"prevOut\":[{\"hash\":\"594692911bbc616737809e0abd991637079501160b1b2eff4e7e0e83f9af4658\"}]}],\"vout\":[{\"value\":\"503890410\",\"addr\":\"9234e37d86AE7De3Dd0Ac57AF815b54551873504\"},{\"value\":\"1900026434448\",\"addr\":\"9234e37d86AE7De3Dd0Ac57AF815b54551873504\"},{\"value\":\"25600\",\"addr\":\"VirtualBurnGas\"}]},\"type\":\"Tx\",\"consensus\":7,\"txType\":99,\"data\":\"{\\\"TxInfo\\\":{\\\"BonusAddrList\\\":3,\\\"BonusAmount\\\":530410958}}\"}","txType":"0","vrfJson":"{}"}}

```



## Transaction information description

- Consensus:  Consensus quantity
- identity:  packer
- time:Trading time
- txHash:hash
- type:The default field is Tx
- utxo
  - multisign:utxo's signature
    - pub:Public key base64
    - sign:Signature base64
  - owner:The originator of the transaction
  - vin
    - prevout
      - hash:Vin's trading hash
    - vinsign:vin's signature
      - pub:Public key base64
      - sign:Signature base64
  - vout
    - addr :The target account for the transfer
    - value :Transfer amount
- verifySign :Transaction signature information
  - pub:Public key base64
  - sign:Signature base64
  - signaddr:Address of the signature node
- txType:Type of transaction
  - 0:Unknown type of transaction
  - 1:Transfer transaction
  - 2:Hypothecation transaction
  - 3:Pledge transaction
  - 4:Invest transaction
  - 5:Disinvest transaction
  - 7:Deployment contract
  - 8:Execution contract
  - 99:Claim transaction
- data
  - Pledge transaction
    - TxInfo Pledge transaction information
      - CommissionRate:Pumping ratio
      - StakeAmount:Amount pledged
      - StakeType:Type of pledge,Net by default
  - Pledge transaction
    - TxInfo Release of pledge transaction information
      - UnstakeUtxo:Utxo of pledge transactions
  - Investment transaction
    - TxInfo Investment transaction information
      - BonusAddr:Investment address
      - InvestAmount:Investment amount
      - InvestType:Investment type. The default value is Normal
  - Investment trading
    - TxInfo Disinvestment transaction information
      - BonusAddr:Investment address
      - DisinvestUtxo:Invest in utxo
  - Claim transaction
    - TxInfo Request trading information
      - BonusAddrList:Number of claims
      - BonusAmount:Amount claimed
  - Deployment contract
    - TxInfo  Deployment Contract information
      - blockPrevRandao:Deployment Contract information
      - blockTimestamp:Contract block time stamp (second unit)
      - input:Contract block timestamp (in seconds)
      - recipient:The sender of the message
      - sender:Recipient of message
      - version:Edition
      - virtualMachine:
        - EVM:0
        - WASM:1
  - Execute a contract
    - TxInfo  Execute Contract information
      - blockPrevRandao:A random number calculated based on the vin of the transaction
      - blockTimestamp:Contract block timestamp (in seconds)
      - contractDeployer:Deployment contract address
      - donation:A tip for the contract deployer
      - input:Execute contract parameters
      - recipient:The sender of the message
      - sender:Receiver of message
      - transfer:Money transferred to the contract
      - version:Edition
      - virtualMachine:
        - EVM:0
        - WASM:1

## Block information description

- blocksign:  Block flow signature
  - pub:  Public key base64
  - sign:Signature base64
  - signaddr:Signed address
- bytes:Block size
- hash:Block hash
- height:Block height
- merkleroot:Merkelgen
- prevhash:Preblock hash
- tx:Transaction information
- data
  - Deployment contract
    - Transaction hash
      - creation:A contract created within a contract
      - dependentCTx:Contractual dependencies
      - output:The binary code of the deployment contract
      - preHash:The pre-hash of the contract
      - storage:storage
  - Execute a contract
    - Transaction hash
      - creation:A contract created within a contract
      - dependentCTx:Contractual dependencies
      - destruction:Destroyed contract
      - log
        - creator:Contract address for generating log
        - data:date
        - topics:topics
      - output:Export of contract
      - preHash:The pre-hash of the contract
      - storage:storage




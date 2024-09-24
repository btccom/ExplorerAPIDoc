# API

## Block

### Block Info

```
GET /block/{xxx}
```

`xxx` can be：

  * Block height
  * Block hash
  * String `latest`
  
#### Examples

  * Get the 3rd block

    <code>[${ENDPOINT}/block/3](${ENDPOINT}/block/3)</code>

  * Get the latest block
    
    <code>[${ENDPOINT}/block/latest](${ENDPOINT}/block/latest)</code>

  * Get the latest and 3rd Block

    <code>[${ENDPOINT}/block/latest,3](${ENDPOINT}/block/latest,3)</code>


### Block List

Get block list by date.

```
GET /block/date/{ymd}
```

#### Examples

  * Get block list on 12/15/2015

    <code>[${ENDPOINT}/block/date/20151215](${ENDPOINT}/block/date/20151215)</code>

### Block Transactions

Batch request is not supported now.

```
GET /block/{xxx}/tx
```

Parameters：

  * `page`, optional, default to `1`
  * `pagesize`，optional, default to `50`, min `1`, max `50`

#### Examples

* Get transactions of Latest block

  <code>[${ENDPOINT}/block/latest/tx](${ENDPOINT}/block/latest/tx)</code>
  
* Get transaction of single block

  <code>[${ENDPOINT}/block/3/tx](${ENDPOINT}/block/3/tx)</code>

## Transaction

### Transaction Info

```
GET /tx/{txhash}
```
      
#### Examples

* Get Single Transaction

  <code>[${ENDPOINT}/tx/0eab89a271380b09987bcee5258fca91f28df4dadcedf892658b9bc261050d96?verbose=3](${ENDPOINT}/tx/0eab89a271380b09987bcee5258fca91f28df4dadcedf892658b9bc261050d96?verbose=3)</code>

### Unconfirmed Tranasction Hash

```
GET /tx/unconfirmed
```

#### Examples

<code>[${ENDPOINT}/tx/unconfirmed](${ENDPOINT}/tx/unconfirmed)</code>
  
### Unconfirmed Tranasctions Summary

```
GET /tx/unconfirmed/summary
```

#### Examples

<code>[${ENDPOINT}/tx/unconfirmed/summary](${ENDPOINT}/tx/unconfirmed/summary)</code>

## Address

### Address Info

```
GET /address/{address}
```

#### Examples

* Get single address
  
  <code>[${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew](${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew)</code>

### Address Transactions

Batch request is not supported now.

```
GET /address/{address}/tx
```

Parameters:

  * `page`, optional, default to `1`
  * `pagesize`，optional, default to `50`, min `1`, max `50`

#### Examples

  <code>[${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew/tx](${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew/tx)</code>

### Unspent

Batch request is not supported now.

```
GET /address/{address}/unspent
```

#### Examples

  <code>[${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew/unspent](${ENDPOINT}/address/15urYnyeJe3gwbGJ74wcX89Tz7ZtsFDVew/unspent)</code>


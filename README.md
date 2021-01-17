# node-pogo-protos
Uses [protobuf.js](https://github.com/dcodeIO/protobuf.js) to compile the Protobuf files from
[POGOProtos](https://github.com/Furtif/POGOProtos) into an easy to use Node module.

<!--
[![npm version](https://badge.fury.io/js/pogo-protos.svg)](https://badge.fury.io/js/pogo-protos)
![npm downloads](https://img.shields.io/npm/dt/pogo-protos.svg) --> 
[![Build Status](https://travis-ci.com/Furtif/pogo-protos.svg?branch=master)](https://travis-ci.com/Furtif/pogo-protos)
![license](https://img.shields.io/npm/l/pogo-protos.svg)


## How to use
```javascript
const POGOProtos = require('pogo-protos');

var myMessage = POGOProtos.Rpc.RecycleItemProto.fromObject({
    item_id: POGOProtos.Rpc.Item.ITEM_POTION,
    count: 50
  });
  
  var encoded = POGOProtos.Rpc.RecycleItemProto.encode(myMessage).finish();
  
  var decodedAgain = POGOProtos.Rpc.RecycleItemProto.decode(encoded);
  console.log(decodedAgain.count); // will print 50
```

For more details see the [protobuf.js documentation](https://github.com/dcodeIO/protobuf.js/wiki).

## Usage with TypeScript
TypeScript definitions are included. Modern IDE should use them automatically.

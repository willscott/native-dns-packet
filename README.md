*This branch exists so that [DNSChain](https://github.com/okTurtles/dnschain) servers can immediately benefit from new features instead of having to wait for them to make it back into the official repo.*

native-dns-packet
-----------------

 * `Packet.parse(buffer)` returns an instance of `Packet`
 * `Packet.write(buffer, packet)` writes the given packet into the buffer,
truncating where appropriate

```javascript
var Packet = function () {
  this.header = {
    id: 0,
    qr: 0,
    opcode: 0,
    aa: 0,
    tc: 0,
    rd: 1,
    ra: 0,
    res1: 0,
    res2: 0,
    res3: 0,
    rcode: 0
  };
  this.question = [];
  this.answer = [];
  this.authority = [];
  this.additional = [];
  this.edns_options = [];
  this.payload = undefined;
};
```

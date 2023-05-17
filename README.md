# Cache-coherence-simulation

This simulation represents how the cache performs to maintain the coherence between two processors using the MSI protocol. This simulation was performed using SMPCache which is a trace-driven simulator for the analysis and teaching of cache memory systems on symmetric multiprocessors.

# the transition diagram for the MSI protocol
`The basic MSI protocol with the Modified, Sharedand Invalid state
`
![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/942a4dcd-10fb-446d-8f55-45dc2afb1db6)


# Results for the first six times of execution


## Accesses number 1

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/d9db00c4-14be-4da1-87a9-65b2bc19459d)

`As we can see, p0 sent a read request because it wanted to read block 273.
first it searched in its cache and didn't find the data so it showed a miss in cache, then it sent a read request on the bus and the bus response with the data from the main memory.`


### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/953ed1a4-56ab-46c4-b146-d9272cfe71ec)

`the state for p0 became shared`

### State Transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/648924c1-1419-47d0-abed-350f43137e33)

`From invalid to shared`

## Accesses number 2

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/0198a09d-4cce-4a1d-9854-165e22077abf)


`p0 sent a read request because it wanted to read block 273.
first it searched in its cache and found the data so it showed ``a hit in cache``.
`
### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/b740ce11-725f-43e5-88e3-b111f1da74c5)

`the state for both p0 and p1 became shared.`

### State Transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/b04cdab2-122d-4408-a374-060ccdae1957)

`From invalid to shared
and now the block is shared for both po and p1
`

## Accesses number 3

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/73b9d137-b9dd-4e26-9a70-f5b270c6e747)

`p0 sent a read request because it wanted to read block 273.
first it searched in its cache and found the data so it showed a hit in cache`

### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/53ff026d-896d-4630-8efd-e41e48ef1264)

`p1 modified the block so it became invalid for p0`

### State Transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/30626399-34f3-4909-8476-6f10dc8c09ec)

## Accesses number 4

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/f3ca98e0-5ffb-49c4-bbbb-4197d16c2506)

`in access number 3 p1 modified the block so it became invalid for p0 that explained why it's no longer in p0 cache.
p0 sent a read request ro the bus and the bus reponse with block transfered from p1. `

### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/17a4daa1-5510-451f-a4c0-3d5cf3e5d357)

`shared for both processors.`

### state transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/96f7aa68-cb35-4313-94b8-da89e84c965d)

`p0 state from invalid to shared`

## Accesses number 5

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/dde55329-815d-4fea-a64f-e750e3baad79)

`p0 found the block in its cache ---> cache hit`

### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/8268fe72-daab-4e91-a419-65ddc24c2fcc)


### State Transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/55d35350-354a-4008-8efa-210a9a324350)

`shared to shared`

## Accesses number 6

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/f3fa528f-a32b-4961-949d-705f66935e30)

`first p0 found the block in its cache ---> cache hit
then p0 modified it
`
### p0 and p1 caches

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/5f4c86ec-9de4-4e73-9c85-74f30872b649)

### State Transition

![image](https://github.com/sondos-gamal/Cache-coherence-simulation/assets/78621105/d3722f10-5cce-4ac1-abb2-2cd9d73ec6f8)



`from shared to modified`

# This project use to test libibverbs API.
## 1. build
        cd ibverebs_API_test
        mkdir build
        cd build
        cmake ../
        make

## 2. server enable
        ./messenger -s

## 3. client enable
        ./messenger -c <ip_addr>
for example:
        ./messenger -c 0.0.0.0

## 4. output
--------------------------
 Server Endpoint
--------------------------
waiting for client connection...
TCP established
ready to send_message: send message
RDMA dev count: 1
RDMA dev name: mlx5_bond_0
ib port num: 1
local id: 0
memory register info: offset=0x7fff353a0608 length=13 lkey=292967 rkey=292967
successed modify QP state to init
send SYNMsg done
recv SYNMsg done
transition to RTR state successfully.
transition to RTS state successfully.
post SR done
completion was found in CQ with status 0x0
Contents of server's buffer at momen: I am client

--------------------------
 Client Endpoint
--------------------------
TCP established
ready to send_message: send message
RDMA dev count: 1
RDMA dev name: mlx5_bond_0
ib port num: 1
local id: 0
memory register info: offset=0x7ffc07dc3698 length=13 lkey=302974 rkey=302974
successed modify QP state to init
send SYNMsg done
recv SYNMsg done
Receive Request was posted
transition to RTR state successfully.
transition to RTS state successfully.
completion was found in CQ with status 0x0
post SR done
completion was found in CQ with status 0x0
get server's buffer context by client: I am server
post SR done
completion was found in CQ with status 0x0


# aaa

estudar sobre as bibliotecas RMI disponíveis para a linguagem de programação escolhida
[a](https://www.youtube.com/watch?v=MZz8iaKxaCw)
[b](https://web.csie.ndhu.edu.tw/showyang/DistrSys2020s/07bRMI.pdf)
Proxy, Skeleton & Servant (?)

Skeleton
• each remote object class has a skeleton that implements the methods in the remote interface
• unmarshals the request message, invokes the corresponding remote object, waits for its completion, and marshals the result

Mechanisms for RMI Delivery
    Guarantees
        Retry request message
        Duplicate filtering
        Retransmission of results

There are Python modules for remote/distributed
objects:
• Pyro  (Python Remote Objects)
• Dopy  (Distributed Objects for Python)
• PyCSP (Communicating Sequential Processes for Python)

[Pyro](https://subscription.packtpub.com/book/application-development/9781785289583/5/ch05lvl1sec63/remote-method-invocation-with-pyro4)

Aula 31/08/2022
Checar se RPC é chamado de RMI pro Python 3
Checar diferenças e aplicações entre
    xmlrpc
    pyro2,3,4,5
    Dopy
    PyCSP

utilizarDoCamelCase

Pra próxima sexta: apresentar as bibliotecas encontradas

Funções mínimas de comunicação
Versão 0.1: N clientes X 1 Servidor

- Cliente
    - id - string
    - chatList - dicionário por pessoa
    * checkMessage () - retorna string (?)
    * sendMessage (remoteId, message) - retorna bool (?)

- Server
    - pendingMessage - dicionário por pessoa
    * receiveMessage (senderId, receiverId, msg) - retorna bool (?)
    * getMessage (id) - retorna string (?)

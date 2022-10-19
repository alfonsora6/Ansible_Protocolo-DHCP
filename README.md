# Práctica: Protocolo DHCP

## Requisitos previos (Modificaciones manualmente en las máquinas kvm/libvirt)

- Tener sudo instalado.

- El usuario principal debe estar configurado en sudoers para poder hacer sudo sin contraseña.

- Tener ssh instalado.

- Tener iptables o network-manager instalado.

- Tener la clave pública importada manualmente.

- Tener configurada la IP estática en la red privada sin DHCP.

## Enunciado de la práctica

Queremos instalar un servidor DHCP en la máquina router para que configure de forma automática las máquinas que se conectan en la red interna. Tenemos que tener en cuenta lo siguiente:

1. La máquina cliente de la práctica anterior, que tiene instalado el servidor web, debe tener la misma IP que la que le asígnate estáticamente, por lo tanto haremos una reserva para que tenga la misma IP.

2. Al añadir una nueva máquina a la red local (recuerda que no se le instalará el servidor web) se configurará de forma dinámica.
    
3. Crea un nuevo rol en el playbook de ansible llamado dhcp que configure el servidor DHCP de forma correcta. Quizás sea necesario modificar el comportamiento de algún rol de la práctica anterior.
    
4. Todos los parámetros que reparta el servidor DHCP, así como cualquier otro dato, por ejemplo la dirección MAC del cliente se guardarán en variables.

5. Añade una nueva máquina al escenario conectada a la red interna muy aislada. Vuelve a ejecutar el playbook y comprueba que todo funciona de forma correcta.

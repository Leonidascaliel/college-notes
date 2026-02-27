Configure um nome para o Switch entrando no modo de configuração [(config#):], utilizando o comando [Hostname] e o nome que você deseja.

### Protegendo o Dispositivo
___
Dispositivos de rede devem ser protegidos contra acessos não autorizados em três frentes:
* Acesso Privilegiado (Modo #)
* Acesso Físico (Console)
* Acesso Remoto (VTY/SSH)

![[Pasted image 20260227101634.png]]
##### Setando password Cisco:
1. Utilize o comando [enable secret class] para setar a senha no sistema.
2. Utilize o comando [line console 0].

##### Alterando IP console Switch
1. Conecte o cabo na entrada RS232 do PC;
2. Conecte a outra ponta do cabo na entrada console do switch;
3. Utilize estes comandos no console:
	`enable`
	`configure terminal`
	`interface vlan 1`
	`ip address 192.168.0.10 255.255.255.0`
	`no shutdown`
	`exit`
	`ip default-gateway 192.168.0.1`
	`end`
	`write memory`
# EJ1

Aplicando VLSM/CIDR, resolver los siguientes escenarios:

a) Dada la red IP 165.10.0.0/22 se necesitan definir:

- 4 (cuatro) redes de 120 hosts:

  7 bits -> 2^7 = 128 dir para cada red.
  | # Red | Dir. Red | Rango hosts | Dir. Broadcast |
  |-|-|-|-|
  | 1 | 165.10.0.0/25 | 165.10.0.1 - 165.10.0.126 | 165.10.0.127 |
  | 2 | 165.10.0.128/25 | 165.10.0.129 - 165.10.0.254 | 165.10.0.255 |
  | 3 | 165.10.1.0/25 | 165.10.1.1 - 165.10.1.126 | 165.10.1.127 |
  | 4 | 165.10.1.128/25 | 165.10.1.129 - 165.10.1.254 | 165.10.1.255 |

- 4 (cuatro) redes de 44 hosts:

  6 bits -> 2^6 = 64 dir para cada red.
  | # Red | Dir. Red | Rango hosts | Dir. Broadcast |
  |-|-|-|-|
  | 5 | 165.10.2.0/26 | 165.10.2.1 - 165.10.2.62 | 165.10.2.63 |
  | 6 | 165.10.2.64/26 | 165.10.2.65 - 165.10.2.126 | 165.10.2.127 |
  | 7 | 165.10.2.128/26 | 165.10.2.129 - 165.10.2.190 | 165.10.2.191 |
  | 8 | 165.10.2.192/26 | 165.10.2.193 - 165.10.2.254 | 165.10.2.255 |

- 8 (ocho) redes de 12 hosts.

  4 bits -> 2^4 = 16 dir para cada red.
  | # Red | Dir. Red | Rango hosts | Dir. Broadcast |
  |-|-|-|-|
  | 9 | 165.10.3.0/28 | 165.10.3.1 - 165.10.3.14 | 165.10.3.15 |
  | 10 | 165.10.3.16/28 | 165.10.3.17 - 165.10.3.30 | 165.10.3.31 |
  | 11 | 165.10.3.32/28 | 165.10.3.33 - 165.10.3.46 | 165.10.3.47 |
  | 12 | 165.10.3.48/28 | 165.10.3.49 - 165.10.3.62 | 165.10.3.63 |
  | 13 | 165.10.3.64/28 | 165.10.3.65 - 165.10.3.78 | 165.10.3.79 |
  | 14 | 165.10.3.80/28 | 165.10.3.81 - 165.10.3.94 | 165.10.3.95 |
  | 15 | 165.10.3.96/28 | 165.10.3.97 - 165.10.3.110 | 165.10.3.111 |
  | 16 | 165.10.3.112/28 | 165.10.3.113 - 165.10.3.126 | 165.10.3.127 |

b) Dada la red IP 4.2.16.0/23 se necesitan definir:

- 1 red de 100 hosts.

  7 bits -> 2^7 = 128 dir
  | # Red | Dir. Red | Rango hosts | Dir. Broadcast |
  |-|-|-|-|
  | 1 | 4.2.16.0/25 | 4.2.16.1 - 4.2.16.126 | 4.2.16.127 |

- 4 (cuatro) redes de 60 hosts

  6 bits -> 2^6 = 64 dir para cada red.
  | # Red | Dir. Red | Rango hosts | Dir. Broadcast |
  |-|-|-|-|
  | 2 | 4.2.16.128/26 | 4.2.16.129 - 4.2.16.190 | 4.2.16.191 |
  | 3 | 4.2.16.192/26 | 4.2.16.193 - 4.2.16.254 | 4.2.16.255 |
  | 4 | 4.2.17.0/26 | 4.2.17.1 - 4.2.17.62 | 4.2.17.63 |
  | 5 | 4.2.17.64/26 | 4.2.17.65 - 4.2.17.126 | 4.2.17.127 |

- Las 5 (cinco) redes se conectan en anillo cada una a partir de un router
  cabecera.

  2 bits -> 2^2 = 4 dir

  Direcciones: 2 para los routers, 1 para la red y 1 para el broadcast. Para cada enlace entre routers.

  | Enlace              | Dir Red       | Router 1   | Router 2   | Broadcast  |
  | ------------------- | ------------- | ---------- | ---------- | ---------- |
  | Router 1 ↔ Router 2 | 4.2.17.128/30 | 4.2.17.129 | 4.2.17.130 | 4.2.17.131 |
  | Router 2 ↔ Router 3 | 4.2.17.132/30 | 4.2.17.133 | 4.2.17.134 | 4.2.17.135 |
  | Router 3 ↔ Router 4 | 4.2.17.136/30 | 4.2.17.137 | 4.2.17.138 | 4.2.17.139 |
  | Router 4 ↔ Router 5 | 4.2.17.140/30 | 4.2.17.141 | 4.2.17.142 | 4.2.17.143 |
  | Router 5 ↔ Router 1 | 4.2.17.144/30 | 4.2.17.145 | 4.2.17.146 | 4.2.17.147 |

c) Dada la red IP 200.23.0.0/20 se necesitan definir:

- 4 (cuatro) redes de 100 hosts.
- 4 (cuatro) redes de 250 hosts
- 2 (dos) redes de 500 hosts.
- Las 10 redes anteriores se conectan cada una de forma individual desde un router spoke contra un router central/hub con conexiones punto a punto.

d) Dada la red IP 160.23.0.0/19 se necesitan definir:

- 20 (veinte) redes de 180 hosts.
- 16 (dieciséis) redes de 90 hosts
- 2 (dos) redes redes de 230 hosts.
- Todas las redes se conectan a una red común de backbone a partir de un
  router cabecera. Para implementar la red central se cuentan con switches de 24 ports+2uplinks.

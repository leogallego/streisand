<p align="center">
  <img src="https://raw.githubusercontent.com/jlund/streisand/master/logo.jpg" alt="Automatizar el efecto"/> 
</p>

- - -
[English](README.md), [Français](README-fr.md), [简体中文](README-chs.md), [Русский](README-ru.md), [Español](README-es.md) | [Mirror](https://gitlab.com/alimakki/streisand)
- - -

[![Build Status](https://travis-ci.org/StreisandEffect/streisand.svg?branch=master)](https://travis-ci.org/StreisandEffect/streisand)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/espadrine.svg?style=social&label=Follow%20%40StreisandVPN)](https://twitter.com/StreisandVPN)

TRANSLATION IN PROGRESS
=========

Streisand
=========

**Silencia la censura. Automatiza el [efecto](https://es.wikipedia.org/wiki/Efecto_Streisand).**

La Internet puede ser un poco injusta. Es muy simple para proveedores de internet, empresas de telecomunicaciones, politicos y corporaciones bloquear el acceso a sitios e información que te interesa. Y atravesar esas restricciones es *dificil*. O no?

Si tienes una cuenta con un proveedor de servicios en la nube (cloud computing), Streisand puede crear un nuevo nodo con multiples servicios de VPN resistentes a la censura de forma casí automatica. Vas a necesitar un poco de experiencia con la linea de comando de Unix (aunque sin Streisand, realizar esta tarea de forma segura podría llevarle días a un administrador Unix experimentado!). Al finalizar, tendrás un sitio web privado con el software y las instrucciones.

Este es **[un ejemplo de un servidor Streisand](http://streisandeffect-demo.s3-website.us-east-2.amazonaws.com/)** y como luce.


Hay una [lista de proveedores de nube soportados](#cloud-providers); aunque expertos puedan utilizar e instalar Streisand en muchos otros.


## Servicios de VPN

Un tipo de herramienta que se utiliza habitualmente para evitar la censura en redes es la Red Privada Virtual (VPN de sus siglás en inglés; _Virtual Private Network_). Hay varios tipos de VPN.

No toda la censura de la red es igual; en algunos lugares esto cambia día a día. Streisand provee distintos tipos de servicios de VPN para evitar distintos tipos de bloqueos o censura. (Y no hace falta instalarlos todos).

Algunos servicios de Streisand incluyen extensiones (add-ons) para proveer mayor resistencia a la censura:

* [OpenSSH](https://www.openssh.com/)
    * [Tinyproxy](https://banu.com/tinyproxy/) puede ser utilizado como un proxy HTTP
* [OpenConnect](https://ocserv.gitlab.io/www/index.html) / [Cisco AnyConnect](https://www.cisco.com/c/en/us/products/security/anyconnect-secure-mobility-client/index.html)
    * Este protocolo es muy utilizado por corporaciones internacionales, y no suele ser bloqueado.
* [OpenVPN](https://openvpn.net/index.php/open-source.html)
    * [Stunnel](https://www.stunnel.org/index.html) extensión disponible.
* [Shadowsocks](https://shadowsocks.org/en/index.html), 
    * [simple-obfs](https://github.com/shadowsocks/simple-obfs) extensión disponible.
* [Tor](https://www.torproject.org/) en modo privado y como puente (bridge relay)
    * [Obfsproxy](https://www.torproject.org/projects/obfsproxy.html.en) con obfs4 disponible como extensión
* [WireGuard](https://www.wireguard.com/), un protocolo moderno y de alta performance.

Leer también:
* Una [lista técnica de caracteristicas](Features.md) 
* Una [lista técnica de servicios](Services.md)

<a id="cloud-providers"></a>
## Proveedores de nube
* Amazon Web Services (AWS)
* Microsoft Azure
* Digital Ocean
* Google Compute Engine (GCE)
* Linode
* Rackspace


#### Otros proveedores
Recomendamos utilizar uno de los proveedores mencionados arriba. Si sos un experto y puedes instalar un servidor Ubuntu 16.04 en otro lado, están las opciones de instalación de "localhost" y "servidor remoto existente". Para mayor información ver [la guía avanzada de instalación](Advanced%20installation.md).

## Instalación

Vas a necesitar acceso a la linea de comando del sistema Unix. Puedes utilizar Linux, BSD, o macOS; en Windows 10, el _Windows Subsystem for Linux_ (WSL) sirve como Linux. 

Una vez que estes listo, lee las [instrucciones completas de instalación](Installation.md).


## Cosas que queremos hacer mejor

Además de una buena limpieza, nos vendría bien:

* Simplificar la instalación
* Adoptar nuevas herramientas anti-censura de forma más rápida

Buscamos ayuda para ambas tareas.

Si crees que hay algo que Streisand debería hacer, o si encontras errores (bugs) en su documentación o ejecución, por favor carga un reporte en el [Sistema de Incidentes](https://github.com/StreisandEffect/streisand/issues).

Cointribuidores Centrales
----------------
* Jay Carlson (@nopdotcom)
* Nick Clarke (@nickolasclarke)
* Joshua Lund (@jlund)
* Ali Makki (@alimakki)
* Daniel McCarney (@cpu)
* Corban Raun (@CorbanR)

Agradecimientos
----------------
[Jason A. Donenfeld](https://www.zx2c4.com/) deserves a lot of credit for being brave enough to reimagine what a modern VPN should look like and for coming up with something as good as [WireGuard](https://www.wireguard.com/). He has our sincere thanks for all of his patient help and high-quality feedback.

We are grateful to [Trevor Smith](https://github.com/trevorsmith) for his massive contributions. He suggested the Gateway approach, provided tons of invaluable feedback, made *everything* look better, and developed the HTML template that served as the inspiration to take things to the next level before Streisand's public release.

Huge thanks to [Paul Wouters](https://nohats.ca/) of [The Libreswan Project](https://libreswan.org/) for his generous help troubleshooting the L2TP/IPsec setup.

[Starcadian's](https://www.starcadian.com/) 'Sunset Blood' album was played on repeat approximately 300 times during the first few months of work on the project in early 2014.

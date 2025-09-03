# Escanear puertos con nmap

<!-- hide -->

> By [@rosinni](https://github.com/rosinni) and [other contributors](https://github.com/4GeeksAcademy/deploying-wordpress-debian/graphs/contributors) at [4Geeks Academy](https://4geeksacademy.co/)

[![build by developers](https://img.shields.io/badge/build_by-Developers-blue)](https://4geeks.com)
[![build by developers](https://img.shields.io/twitter/follow/4geeksacademy?style=social&logo=twitter)](https://twitter.com/4geeksacademy)

*These instructions are [available in english](https://github.com/breatheco-de/scan-with-nmap-practice/blob/main/README.md)*
<!-- endhide -->


<!-- hide -->


### Antes de empezar...

> ¡Te necesitamos! Estos ejercicios se crean y mantienen en colaboración con personas como tú. Si encuentras algún error o falta de ortografía, contribuye y/o repórtalo.

<!-- endhide -->

## 📋 Propósito del Proyecto

Este proyecto está diseñado para enseñar los fundamentos de seguridad de redes a través de la práctica con Nmap (Network Mapper). Los estudiantes aprenderán a:

- Realizar reconocimiento de redes y evaluación de vulnerabilidades
- Identificar hosts activos y puertos abiertos en sistemas objetivo
- Descubrir servicios en ejecución y sus versiones
- Buscar potenciales vulnerabilidades de seguridad
- Generar reportes profesionales de vulnerabilidades
- Comprender las debilidades de seguridad de red y sus implicaciones

## 🛠️ Tecnologías Utilizadas

- **Nmap** - Herramienta de escaneo de redes y auditoría de seguridad
- **Kali Linux** - Distribución para pruebas de penetración y auditoría de seguridad (máquina escaneadora)
- **Debian Linux** - Sistema operativo objetivo para evaluación de vulnerabilidades
- **Bash/Shell** - Interfaz de línea de comandos para ejecutar escaneos
- **Máquinas Virtuales** - Tecnología de virtualización para entorno de pruebas seguro
- **Bases de Datos CVE** - Bases de datos públicas de vulnerabilidades (NVD, CVE Details, Exploit-DB, Vulners)

## 🚀 Cómo Instalar y Ejecutar

### Prerrequisitos
* Máquina virtual con Kali Linux (máquina escaneadora)
* Máquina virtual con Debian (máquina objetivo)
* Conocimiento básico de línea de comandos de Linux
* Conectividad de red entre ambas máquinas

### Instalación

1. **Configurar tus máquinas virtuales:**
   - Asegúrate de que tanto Kali Linux como Debian estén ejecutándose
   - Configura la conectividad de red entre las máquinas
   - Anota la dirección IP de tu máquina Debian objetivo

2. **Instalar Nmap en Kali Linux (si no está instalado):**
   ```bash
   sudo apt-get update
   sudo apt-get install nmap
   ```

3. **Clonar este repositorio:**
   ```bash
   git clone https://github.com/[tu-usuario]/scan-with-nmap-practice.git
   cd scan-with-nmap-practice
   ```

### Pasos de Ejecución

## 📝 Instrucciones de Práctica

### Comenzando

1. **Haz fork de este repositorio:**
   * Abre esta URL: https://github.com/breatheco-de/scan-with-nmap-practice
   * Haz clic en el botón Fork para crear una copia en tu cuenta de GitHub

   ![botón fork](https://github.com/4GeeksAcademy/4GeeksAcademy/blob/master/site/src/static/fork_button.png?raw=true)

2. **Clona tu repositorio forkeado:**
   ```bash
   git clone https://github.com/[tu-usuario]/scan-with-nmap-practice.git
   cd scan-with-nmap-practice
   ```


### Paso 1: Escaneo con Nmap
En la maquina kali realizaremos un escaneo con Nmap para descubrir los hosts activos y los puertos abiertos en una red o en un dispositivo específico.

- [ ] **Instalación de Nmap (si no está instalado):**
```bash
sudo apt-get install nmap
```

- [ ] **Escaneo básico de un objetivo (IP de la máquina Debian <IP_debian>):**
```bash
nmap <IP_debian>
```

### Paso 2: Enumerar Puertos y Verificar Servicios
Después de realizar el escaneo, Nmap proporcionará una lista de puertos abiertos y los servicios que operan en esos puertos.

- [ ] **Escaneo de puertos y servicios:**
```bash
nmap -sV <IP_debian>
```
> Esta opción (-sV) permite detectar la versión del servicio que está operando en cada puerto.

- [ ] **Escaneo detallado y búsqueda de vulnerabilidades:**
```bash
nmap -sV --script=vuln <IP_debian>
```
> La opción (--script=vuln) ejecuta scripts de detección de vulnerabilidades que Nmap tiene incorporados.

### Paso 3: Documentar Vulnerabilidades Asociadas a los Servicios

- [ ] **Anota los Servicios y sus Versiones:** Del resultado del escaneo, toma nota de los servicios y sus versiones. Por ejemplo:
    * Apache 2.4.7
    * OpenSSL 1.0.1f
    * OpenSSH 6.6.1p1

- [ ] **Buscar Vulnerabilidades en Bases de Datos Públicas:** Utiliza bases de datos públicas de vulnerabilidades para buscar información sobre los servicios detectados. Las siguientes son las fuentes más comunes:
    * NVD (National Vulnerability Database): https://nvd.nist.gov/
    * CVE Details: https://www.cvedetails.com/
    * Exploit Database: https://www.exploit-db.com/
    * Vulners: https://vulners.com/

> 💡Ejemplo: Para el servicio Apache 2.4.7, ve a la página de NVD: https://nvd.nist.gov/ e
ingresa "Apache 2.4.7" en la barra de búsqueda.

- [ ] **Documenta las vulnerabilidades de manera estructurada.** Aquí tienes un ejemplo de cómo documentar una vulnerabilidad:

![reporte de vulnerabilidad](https://github.com/breatheco-de/scan-with-nmap-practice/blob/main/assets/report-vul-es.png?raw=true)

## 📤 Entrega de Proyecto

* Sube tu reporte de vulnerabilidades en formato `.pdf` a la raíz de tu repositorio forkeado con el nombre `vulnerability-report.pdf`.
* Asegúrate de que tu reporte incluya:
  - Servicios identificados y sus versiones
  - Números CVE y descripciones
  - Evaluación de riesgo para cada vulnerabilidad
  - Recomendaciones para remediar las vulnerabilidades

## 📚 Recursos Adicionales

- [Documentación Oficial de Nmap](https://nmap.org/docs.html)
- [Base de Datos Nacional de Vulnerabilidades](https://nvd.nist.gov/)
- [CVE Details](https://www.cvedetails.com/)
- [Base de Datos de Exploits](https://www.exploit-db.com/)
- [Mejores Prácticas de Seguridad de Red](https://www.nist.gov/cybersecurity)



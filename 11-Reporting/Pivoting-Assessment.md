# Pivoting Assessment

## Objective

Demonstrate access to an isolated internal network through a compromised Windows host.

## Pivot Host

Windows 10:

- Attacker-facing network: `192.168.88.136`
- Internal network: `10.10.10.128`

## Internal Target

Metasploitable 2:

- Internal IP: `10.10.10.130`

## Pivot Method

A Meterpreter session was established on the Windows host.

An internal route was configured:

10.10.10.0/24

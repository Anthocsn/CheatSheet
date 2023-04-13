# Nmap

`nmap -sS -Pn -p- target`

* -sS : Syn Scan (Stealth)
* -Pn : For skip ping (If we know the target and ping is blocked for example)
* -p- : All ports.
* -p : 1-65535 or 80,443
* -oN : Output in normal format
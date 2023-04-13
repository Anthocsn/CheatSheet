# Dirbuster

`dirbuster -e "html,php,asp,aspx,txt" -u "http://target:80" -R -l wordlist `

## Default options

* -e : File extention (html,php,asp,aspx,txt...)
* -u : URL
* -l : Worlist

## Others options

* -r : For save the report
* -s : Change the start point. Default: /
* -R : Don't be recursive. Faster for first scan.
* -H : No GUI (Not working for me, can't find anything)
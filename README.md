# chro.in

Page to test hostinger service without SSL and check if adding 3rd party SLL certificate is possible.

**Steps:** 

- Host gh page @ https://inf800.github.io/chro.in
- Create `CNAME` file with `www.chro.in`. (This will redirect all browsers to www.chro.in whe https://inf800.github.io/chro.in is given in URL field)
- Add the following in DNS / Nameservers: (Same cane be done for other providers like godaddy etc.)
  | Type | Name | Content | TTL |
  | --- | --- | --- | --- |
  |A|@|185.199.108.153|14400|
  |A|@|185.199.109.153|14400|
  |A|@|185.199.110.153|14400|
  |A|@|185.199.111.153|14400|

  

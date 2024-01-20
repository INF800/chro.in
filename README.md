# chro.in

Page to test hostinger service without SSL and check if adding 3rd party SLL certificate is possible.

#### Steps to direct chro.in to github pages (HTTP)

- Host gh page @ https://inf800.github.io/chro.in
- Create `CNAME` file with `www.chro.in`. (This will redirect all browsers to www.chro.in when https://inf800.github.io/chro.in is given in URL field)
- Add the following in DNS / Nameservers: (Same cane be done for other providers like godaddy etc.)
  | Type | Name | Content | TTL |
  | --- | --- | --- | --- |
  |A|@|185.199.108.153|14400|
  |A|@|185.199.109.153|14400|
  |A|@|185.199.110.153|14400|
  |A|@|185.199.111.153|14400|

  Now, chro.in will contain the contents deployed at https://inf800.github.io/chro.in.

#### Steps to add SSL (HTTPS)

- Signup @ https://www.cloudflare.com/
- Click on "Add website or application"
- Enter domain name "chro.in" and press continue. 
- Select free tier
- Verify DNS records are set correctly. You should see previously added information automatically. Press continue.
  <img width="674" alt="image" src="https://github.com/INF800/chro.in/assets/45640029/c598c209-15d8-4922-84c9-069f26da5303">
- Ignore the next page that tells you to do 1. Log in to your domain registrar, 2.Avoid DNS resolution issues caused by DNSSEC and 3. Update your nameservers. Press continue.
- Go to the "SSL/TLS" section.
- Choose the SSL/TLS encryption mode to "Full (strict)". That's it. (If it is not updated, set it to "Off (not secure)" and back to "Full (strict)" and see results at chro.in.

> #### References
> - https://dev.to/vjnvisakh/hosting-a-custom-domain-on-github-2d1a
> - https://dev.to/pratik_kale/github-pages-custom-domains-and-ssl-mc4

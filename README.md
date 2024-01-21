# chro.in

Page to test hostinger service without SSL and check if adding 3rd party SLL certificate is possible.

#### Steps to direct chro.in to github pages (HTTP)

- Host gh page @ https://inf800.github.io/chro.in
- Create `CNAME` file with `www.chro.in`. (This will redirect all browsers to www.chro.in when https://inf800.github.io/chro.in is given in URL field)
- Add the following in DNS / Nameservers: (Same can be done for other providers like godaddy etc.)
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
- Select the free tier
- Verify DNS records are set correctly. You should see previously added information automatically. Press continue.
  <img width="674" alt="image" src="https://github.com/INF800/chro.in/assets/45640029/c598c209-15d8-4922-84c9-069f26da5303">
- The next page that tells you to do 1. Log in to your domain registrar, 2. Avoid DNS resolution issues caused by DNSSEC and 3. Update your nameservers (follow them and). Press continue.
  1. Log in to your domain registrar
    > "Domain registrar" is the same as your domain provider like Hostinger, GoDaddy, etc.
  2. Avoid DNS resolution issues caused by DNSSEC
    > Basically delete all DNSSEC fields
  3. Update your nameservers
    > Replace your provider's nameservers with cloudfare's nameserver
- Go to the "SSL/TLS" section.
- Choose the SSL/TLS encryption mode to "Full" (Do not select the "Full (strict)" which will cause [526](https://developers.cloudflare.com/support/troubleshooting/cloudflare-errors/troubleshooting-cloudflare-5xx-errors/#error-526-invalid-ssl-certificate) with cloud fare).
- Wait for a 24-48 Hrs, you should be able to see secure https connection @ https://www.chro.in/


> #### References
> - https://dev.to/vjnvisakh/hosting-a-custom-domain-on-github-2d1a
> - https://dev.to/pratik_kale/github-pages-custom-domains-and-ssl-mc4
> - https://stackoverflow.com/questions/54059217/how-to-fix-domain-does-not-resolve-to-the-github-pages-server-error-in-github
> - https://developers.cloudflare.com/support/troubleshooting/cloudflare-errors/troubleshooting-cloudflare-5xx-errors/#error-526-invalid-ssl-certificate

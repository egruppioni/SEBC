[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log
 
[libdefaults]
default_realm = EGRUPPIONI.HQ
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = arcfour-hmac
default_tkt_enctypes = arcfour-hmac
permitted_enctypes = arcfour-hmac
udp_preference_limit = 1
kdc_timeout = 3000

[realms]
EGRUPPIONI.HQ = {
kdc = 10.100.7.16
admin_server = 10.100.7.16
}

[domain_realm]
   .example.com = EGRUPPIONI.HQ
   example.com = EGRUPPIONI.HQ
   
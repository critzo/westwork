FROM resin/rpi-raspbian:jessie

MAINTAINER Ross Schulman

RUN apt-get update && \
	apt-get install -y slapd ldap-utils

VOLUME ["/etc/ldap"]
VOLUME ["/var/lib/ldap"]

EXPOSE 389

CMD ["slapd", "-h", "ldap:///", "ldapi:///", "-g", "openldap", "-u", "openldap", "-F", "/etc/ldap/slapd.d"]

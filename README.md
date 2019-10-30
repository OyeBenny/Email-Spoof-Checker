# Email-Spoof-Checker

The script is requesting DNS records for the host, analyzing the settings on the DMARC/DKIM/SPF and then based on those results it tells you if it's spoofable.

In other words, it checks to see if a domain can be utilized to send spoofed emails. IT JUST CHECKS. You put a list of domains into a file and you run it.

You would want to use it on a bunch of different root domains, not subdomains.   

The domain, although it can be spoofed, most domains can be spoofed, but they will go to spam - due to the root domain's DMARC policy. You can have either "Allow", "Quarantine", "Reject". The only one that actually prevents it is reject, but quarantine is what usually happens.

To Run: python spoofcheck.py scope.txt

# NOOB
        A script to find subdomains of a given domain:
        
    chat GPT and i are now married
    GPT is now my grandmother im now its kilt
    i have no clue what the uk im doing but i have a raspberry pi ,stims and floppy isk.0
    anyhelp or some ganja would be welcomed 
    MetallicA fkn RULE. 
    JA RULE...
    YA TOOL
    
import dns.resolver

def find_subdomains(domain):
    resolver = dns.resolver.Resolver()
    resolver.nameservers = ["8.8.8.8"]  # Use Google's DNS servers
    subdomains = []
    try:
        answers = dns.resolver.query(domain, "NS")
        for rdata in answers:
            subdomains.append(str(rdata))
    except:
        pass
    return subdomains

# Example usage
domain = "example.com"
subdomains = find_subdomains(domain)
print(f"Subdomains of {domain}: {subdomains}")

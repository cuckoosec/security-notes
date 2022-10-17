Web
BuiltWith
Wappalyzer
Shodan

https://www.theosintion.com/practical-social-engineering/

```
recon-ng -w walmart
workspace [load | create | remove] walmart
marketplace search 
# To search for modules

marketplace install import/csv_file
marketplace install all

keys add name_of_module value 
# For API keys
keys list

# TO search for a module of specific type
modules search discovery
module load metacr # metacrawler module

options set SOURCE nostarch.com
options set extract true

```

#### Enumerating Files with Metacrawler

The `metacrawler` module searches a target site or sites for Microsoft PowerPoint, Word, Excel, and PDF files. It’s the equivalent of doing a _Google dork_—writing long search queries, like this:

```
site:nostarch.com Filetype:XLS* OR Filetype:DOC* OR Filetype:PPT* or Filetype:PDF
```

If `Extract` is set to `True`, this command outputs all documents on the target’s public website that are in PDF or Microsoft Office formats (Excel, Word, or PowerPoint) with a link to the file and metadata, including the author, the software that created it, the modification date, the software that produced it, and the date on which it was created. If `Extract` is set to `False`, the output provides the filename and link only.

Given this information, you can do numerous things. From the metadata, you can enumerate users, operating systems, and software Given this information, you can do numerous things. From the metadata, you can enumerate users, operating systems, and software used. From the files themselves, you might be able to find information the target intended to keep private, including names, email addresses, phone and fax numbers, locations, and important business matters.

The `whois_pocs` module enumerates all known points of contact for a given domain. It’s more robust for this feature than the `whois_miner` module and works even against targets with domain privacy. Here is an example of running this module against Walmart:

he SPF record lists domain verifications for Adobe, Facebook, DocuSign, Microsoft, and Google. The text (TXT) record that begins with `MS=` indicates that Walmart uses Microsoft Office 365 6. It also uses `adobe-idp-site-verification` to validate domains for Adobe Enterprise products like Creative Cloud 4. The `facebook-domain-verification` TXT record restricts the domains that edit the official Facebook page for the domain 3. The TXT record that begins with `docusign=` indicates that the site uses DocuSign to sign official documents 5.


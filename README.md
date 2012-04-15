GPG email search utility
========================

Command line utility to search for GPG keys on http://pgp.mit.edu by email addresses.

Interface
---------

* **stdin**: search queries, one per line
* **stdout**: the search results, if any, in HTML format
* **stderr**: a message for each search that yields no results

Example
-------
Example with email_list.txt containing email addresses, one per line:

    ./gpg-email-search < email_list.txt | tee results.html

Example input (email_list.txt):

    test@example.org

Example output (results.html):

    <!DOCTYPE HTML>
    <html><body><pre>
    pub  1024D/<a href="http://pgp.mit.edu:11371/pks/lookup?op=get&search=0x1F9D0C0240801C06">40801C06</a> 2009-03-22 <a href="http://pgp.mit.edu:11371/pks/lookup?op=vindex&search=0x1F9D0C0240801C06">Noam Sayn (No Comment) &lt;fake@example.org&gt;</a>
    pub  2048R/<a href="http://pgp.mit.edu:11371/pks/lookup?op=get&search=0xDB3BF13F3C1F2E89">3C1F2E89</a> 2009-03-16 <a href="http://pgp.mit.edu:11371/pks/lookup?op=vindex&search=0xDB3BF13F3C1F2E89">locksley mendoza (fake addy for keyserver spambots) &lt;fake@example.org&gt;</a>
    </pre></body></html>

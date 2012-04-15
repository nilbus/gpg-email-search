GPG email search utility
========================

Command line utility to search for GPG keys on pgp.mit.edu.

Despite the name, search keys don't have to be email addresses; you can also search by name and comment.

Uses an exact match search.

**stdin**: search queries, one per line
**stdout**: the search results, if any, in HTML format
**stderr**: a message for each search that yields no results

Example
-------
Example with email_list.txt containing email addresses, one per line:

    gpg-email-search < email_list.txt | tee results.html

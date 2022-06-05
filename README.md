# Description
Looking for a free and secure network drive to store personal data across
devices on the Internet, I was not convinced by many things. The locations of
the data centers, unclear data protection and security, poor performance...
Powerful mailboxes with IMAP support are easier to find. And so the idea was
born to implement a shared and fully encrypted network drive based on IMAP.

For Windows, the project provides a corresponding service that is configured for
a directory on the local PC and a mail account. The service creates an
additional directory in the mail account, in which all files and directories of
the local directory are synchronized. The file contents as well as the meta data
are stored completely encrypted in the mail account. Only the client(s) with the
appropriate key can decrypt them, which the service implemented here can do, and
a normal local synchronized directory then exists for the user, which he can use
as usual.

Concurrent accesses are handled very simply -- whoever writes last wins.

If the service or the mail account is not accessible, all files are read-only.

# Time Synchronization

## Explanation

Time synchronization in the context of log ingestion refers to the alignment of clocks on all logging devices.  

## Importance

Without time synchronization it would be virtually impossible to track events through a system, it would be unclear whether events logged in two places refer to one and the same event or if the same event happened twice.  

## Example

A well known example of hacking comes from Cliff Stoll's 1989 book, *The Cuckoo's Egg* detailing his endeavours in tracking down a hacker after noticing 9 seconds of unaccounted computing time on a UNIX mainframe Lawrence Berkeley National Laboratory.  While these 9 seconds may have been noticed in the isolated LBL UNIX machine, as Stoll tracked the hacker the need to know his progression through different systems relied heavily on the synchronization of the various machines to show where the hacker moved and when.  

## Additional Resources

- [Stalking the Wily Hacker](http://pdf.textfiles.com/academics/wilyhacker.pdf) - Clifford Stoll's abridged account of his hunt for the LBL hacker
- [Netsurion](https://www.netsurion.com/articles/5-cyber-security-myths-importance-of-time-synchronization-and-more) - a brief explanation of time synchronization with more resources in footnotes

# Operation7 Latino Clauncher
# Operation7 Clauncher
# Operation7 Latino Launcher
# Operation7 Launcher
Operation7 Game Launcher with Login and Auto-Save.

[Theoretical Context]
Operation7 was created by ParkESM, likely around 2003 or 2006.

The story goes that its founders were former employees who had worked on the *Lineage 2* series at NCSOFT. Following a mass layoff of programmers, they founded ParkESM, utilizing the same technology, concepts, and even the same distributor—a fact kept from the public due to a specific contractual clause.

Later on, Tencent and other companies would adopt a similar style of "launcher"—a functionality popularized by these large-scale games.

[The code linking *Lineage 2* and Operation7]
Within the internal code of Operation7, there appears a component known as "INET," which refers to the internal netcode—essentially the launcher itself.

The launcher hashes your password using MD5 and performs CRC32 checksums on the files via "Updater.exe" to ensure they are not corrupted.

It passes parameters such as:
Operation7.exe INET [Username] + [Password (MD5)] + [Age (+18)]

Upon startup, it sends the username and password via an API to a web server, which responds with a date and time value—acting as a "salt" for the password.

[How did I obtain this?]
In 2014, I gained access to the database of the company Axeso5 by exploiting a flaw in their security system, and I subsequently published the findings on my Facebook page. I decrypted the code—which had been encrypted by a third-party firm (likely named something like "GearCode," a company that provided robust protection for many years).

However, the reverse engineering of the network protocol was relatively straightforward; tools like "Charles Proxy" were used to capture traffic, revealing the parameters sent to the web API, as well as the internal "INET" component triggered when the game was run with administrator privileges. And I ended up creating this functional project in 2014; it is now obsolete following the change of company from Axeso5 to Softnyx.

<img width="1018" height="739" alt="image" src="https://github.com/user-attachments/assets/45b6ff2f-9b27-4ffe-9b8e-d88a442b8fba" />

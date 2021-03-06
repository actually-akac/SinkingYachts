# Sinking Yachts 🐟

<div align="center">
  <img width="256" height="256" src="https://cdn.discordapp.com/icons/908947284853682266/a928bf7a58ed5fccbdbadefd0aee34ff.png?size=256">
</div>

<div align="center">
  A C# library for detecting Discord/Steam phishing links using the Sinking Yachts API. 
</div>

## Usage
This library can be downloaded as the package `SinkingYachts`. The main class is called `YachtsClient`.

https://www.nuget.org/packages/SinkingYachts

## Features
- Fully async
- Access to a Discord-related phishing database of over `13 300` confirmed malicious domains
- Regex matching of domains and automatic phishing detection
- Different modes for storing and loading phishing domains
- Instant updates through **WebSocket events**
- Domain whitelisting to prevent false positives
- Customizable caching to decrease load 

## Available methods
- Task<Change[]> `Recent`(TimeSpan time)
- Task<Change[]> `Recent`(int seconds)
- Task<bool> `IsPhishing`(string content)
- Task<bool> `IsPhishingDomain`(string domain)
- Task<int> `DatabaseSize`()
- Task<string[]> `GetPhishingDomains`()

## Available events (requires `StorageMode.LocalWS`)
- EventHandler\<string> `DomainAdded`
- EventHandler\<string> `DomainDeleted`  

## Statistics from the past week
| Date | New domains found |
| :---: | :---: |
| 23.07.2022 | + `32` |
| 24.07.2022 | + `30` |
| 25.07.2022 | + `54` |
| 26.07.2022 | + `39` |
| 27.07.2022 | + `15` |
| 28.07.2022 | + `25` |
| 29.07.2022 | + `46` |

## Recently flagged domains
```ruby
steamcommunityoa.top
steamcommunltty.ru
steamcommunityev.top
stearncommumity.ru
discold-giftk.xyz
dilscordilgipz.com
discrod-ez-gifts.com
join-hypesquads-group.ml
join-hypesquads-team.com
join-events.ml
hype-team.tk
```

## Example
Under the `Example` folder you can find a demo Discord bot that implements this library.
```rust
18.06. 20:09:38 [Discord] Discord.Net v3.6.0 (API v9)
18.06. 20:09:38 [Gateway] Connecting
18.06. 20:09:40 [Gateway] Connected
18.06. 20:09:40 [Bot] Bot is ready to protect your server from 13326 phishing domains
18.06. 20:09:40 [Bot] Domains added within the past day: 111
18.06. 20:09:40 [Bot] Domains deleted within the past day: 0
18.06. 20:09:40 [Gateway] Ready
```
  
## Unknown domains
Found a Discord/Steam phishing domain that isn't yet present in the database? Send it into the `#domain-reports` channel on our Discord server or open an **issue**. 
  
## Links
Need help, want to discuss phishing or have a suggestion? Feel free to join our Discord server: https://discord.gg/d63pvY28HU

Official website: https://sinking.yachts<br>
Email: sinkingyachts@gmail.com<br>
GitHub: https://github.com/SinkingYachts<br>
Blog: https://sinking.yachts/blog/<br>

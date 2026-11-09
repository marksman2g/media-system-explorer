
# Your Media System
## Two complete paths. One clear decision framework.
**Prepared for Tony • October 7, 2026 • Version 1.1**

> **My recommendation:** solve the external-provider account problem first, without buying a NAS. For media you decide to keep, use a ten-drive NAS as storage and a separate Intel graphics-capable computer as the media server. Present both NAS units through one media library when you expand—not one fragile pool stretched across boxes.

This is a completed research and design package, not a claim that hardware has been purchased, software has been installed on your computer, or customer accounts have been provisioned. The offline explorer, printable map and narration are ready to use. Live deployment still requires the chosen equipment, authorized provider access and validation on your actual playback devices. No credentials, device activations, purchases or account changes were made.

**How to read this:** modules 1–3 settle the external-server decision; modules 4–8 cover obtaining and owning files, including the added torrent/Reddit section 4A; modules 9–11 cover playback, tools and acceptance tests. Prices are US dollars before tax unless marked otherwise. A **listed price** came from a retrieved sales page; an **allowance** is a planning estimate, not a live offer. A vendor platform listing is not a laboratory test of every model, codec or subtitle format.

## 1. The complete system, without unnecessary storage

| Layer | External server / provider | Your own files / server |
|---|---|---|
| Obtain access or content | Provider authorizes an account, device or playlist. Content remains upstream. | Receive an authorized file, make an allowed recording, or digitize material you have the right to copy. |
| Storage | Usually **none at your home** beyond app cache. Provider stores files or distributes live channels. | Intake folder → verified file → media folders on NAS → protected copies of important material. |
| Organization | Provider supplies catalog and guide. Your player may organize favorites and playlists. | Metadata, names, posters, seasons, languages and subtitles are maintained by your server and optional tools. |
| Identity and control | Provider account system is authoritative. Player activation is a separate layer. | Your Jellyfin/Emby administrator or Plex sharing configuration controls permitted libraries and users. |
| Delivery | Upstream internet upload → your/customer internet download → player. | NAS → media server → local network, or your internet upload → remote player. |
| Your responsibilities | Device/app support, individual entitlements where delegated, payment/licensing terms and provider escalation. | Storage health, updates, backups, server operation, security and bandwidth. |
| Best use | Watch without maintaining a large collection. Manage authorized customers only where provider contract and tooling allow it. | Preserve your media, control your library, and operate independently of a provider's catalog. |

These are separate architectures, not successive mandatory stages. A hybrid simply puts both kinds of app on the same television. It does **not** turn Netflix, Tubi or an upstream IPTV account into files that Sonarr or Jellyfin can automatically own. Player, server and account manager are three different jobs. [F1](#source-F1)[J1](#source-J1)[P1](#source-P1)[A10](#source-A10)

### The simplest usable flows

**External:** licensed provider → individually authorized customer account → compatible player → television/phone. Optional player-management console sits beside this flow; the upstream system still grants or denies content.

**Owned:** approved source → intake/verification → named NAS media folders → Jellyfin or Plex on the serving computer → playback apps. Backups cover irreplaceable files and server configuration. Optional automation sits between intake and the final library.

**Hybrid:** keep both flows. Use a common home-screen layout and a written source label—“My library” versus “Provider”—rather than attempting to merge incompatible authentication systems.

## 2. External servers: the control problem comes before the app

### What Flix Pro is—and is not

The matching product is **Flix Pro Player**, with playlist, activation and reseller entry points. That is not proof that its device-activation console controls your provider's underlying service accounts. “Lifetime” activation can describe the app license, not lifetime content, permanent provider access or a guaranteed number of concurrent streams. Your exact upstream contract and dashboard were not inspected in this research. [F1](#source-F1)

Three limits must be tracked separately: **registered devices**, **simultaneous stream connections**, and **paid player activations**. Five registered devices is not the same as five concurrent streams. A recording or multi-view window may consume another stream; the provider must define how it counts sessions.

### Can one five-connection account become five independently controlled assignments?

| Arrangement | What you can assign | Disable just customer C? | Important consequence |
|---|---|---|---|
| Same provider username/password on five devices | A convenient label for each device, not five independent identities | **Not reliably.** Removing C's local playlist is not server-side revocation. | Anyone retaining the URL/password may reconnect. Rotating the shared password interrupts everyone. |
| Five different player activation licenses, same provider login | Five app licenses | You may alter an app entitlement, but that does not revoke the copied upstream credential. | The customer may use a different player. App licensing is not content security. |
| Provider creates five subaccounts, each one stream | Five real identities, preferably with separate expiration, password and session controls | **Yes, when the provider grants you those controls.** | This is the recommended external architecture. Provider must permit the arrangement contractually. |
| Provider binds five independent device tokens/MAC registrations | Five provider-enforced device assignments | **Yes, only if revocation is enforced upstream per device/token.** | A MAC address alone is not a strong secret; test Wi-Fi/Ethernet changes and replacement devices. |
| Authorized managed gateway hides a shared upstream secret | Your gateway identities and session rules | Potentially, if every stream must traverse and be authorized by the gateway | Requires explicit upstream permission, secure token design, relay bandwidth and administration. It is not created by installing a player. |
| Provider exposes no individual control and will not cooperate | Only the shared account | **No secure independent revocation available.** | Buy genuinely separate accounts or use a different authorized provider; do not promise customers isolation you lack. |

The table's revocation analysis follows from where authentication is enforced. A playlist editor changes what a player sees; it is not necessarily on the path when a previously copied stream URL is opened. SS IPTV's operator integration, for example, explicitly requires an operator-side authorization service. [F9](#source-F9) A successful login-denial test is still not enough: the provider must also explain whether an already running stream stops, and whether old refresh tokens or URLs remain valid.

### The five-assignment operating design

Use customer identifiers **A through E**, each mapped to its own upstream account/token, allowed device(s), one-stream entitlement, expiration, app activation and support notes. Never put passwords in this report, the offline explorer or a customer spreadsheet. Store secrets in a protected password manager. A customer with two televisions may need two registered devices but only one concurrent stream—or two paid entitlements—depending on the provider.

**Required provider deliverables:** explicit permission for the intended household/customer arrangement; five distinct credentials or revocable device identities; delegated portal/API to create, suspend, reset and terminate sessions; visible concurrent-use and device limits; supported endpoints and EPG; clear replacement-device and outage policy. A generic reseller button is not evidence that a particular subscription supports all of this.

**Acceptance test:** start streams A–E on distinct authorized identities; suspend C; verify C cannot start a new stream and its existing session is handled as documented; confirm A, B, D and E continue; rotate C's credential; test that its old credential fails; restore C. Then test a sixth concurrent connection and record the provider's actual behavior. This is the standard for calling the system independently managed.

### Diagnosing the current Flix issue without buying another license blindly

Use one lawful test source on the same device and network in Flix and a second compatible player. If both fail, investigate provider availability, expired credentials, stream limits, EPG and network path first. If only Flix fails, the player, saved profile or codec support is a better suspect. Separately compare wired networking with Wi-Fi, and PIA on versus off where the provider permits both. Record time, device model, app version, channel/title, error, active streams and whether failure affects only that device. Do not run many simultaneous tests on a one-connection account.

## 3. Ten alternatives in the same playback category

All ten below can act as **clients for externally supplied media streams or playlists**. None includes a legal content catalog simply because it is installed. VLC and Kodi are broader media players, not one-for-one Flix activation dashboards; that distinction is explicit. Plex, Jellyfin and Emby are compared separately because they are server ecosystems, not disguised substitutes for an upstream IPTV reseller panel.

**Ordering:** genuinely free options first, then freemium, then paid options. Within paid products, management suitability matters more than marketing claims. No reviewed free player simultaneously provides universal device coverage, a verified Flix-style activation console, and secure independent subdivision of one shared provider account.

| Rank / product | Category fit and verified platform scope | Price status | Your management requirement |
|---|---|---|---|
| 1. **VLC** | Free general network/file player; Windows, macOS, Linux, Android, iOS; TV editions depend on platform. Broader than Flix, weaker TV-guide experience. | Free/open source. Official site retrieval was limited; exact current TV-store availability not revalidated. | No customer provisioning or upstream revocation. Useful independent playback test. [F8](#source-F8) |
| 2. **Kodi + IPTV PVR client** | Free media-center front end; official builds for Windows, Linux, macOS, Android, iOS, tvOS and webOS. Some Apple/webOS installation paths are not simple app-store installs. | Free/open source; content and any separate backend are not included. | Local profiles/EPG are not provider subaccounts. No native Flix-style customer activation console. [F7](#source-F7) |
| 3. **IPTVnator** | Purpose-built playlist/EPG client; Windows, macOS, Linux and browser/PWA. M3U, provider API/portal support documented. Not a native Roku/TV universal solution. | Free/open source. | No reseller or central customer revocation system. Strong free desktop shortlist. Browser codec/CORS restrictions may differ from desktop. [F6](#source-F6) |
| 4. **SS IPTV** | Smart-TV IPTV player; selected Samsung/LG and other supported models, not a guarantee for every current TV/store region. | Free player. | Playlist management and operator integration exist. Real customer authentication requires your provider/operator backend. Conditional, not turnkey account splitting. [F9](#source-F9)[F10](#source-F10) |
| 5. **Televizo** | Android phone, tablet and TV playlist player. Not an iOS/Roku alternative. | Free basic tier; Premium is paid. Exact current upgrade price not confirmed. | Local playlist control, not independent provider accounts or a verified reseller console. [F5](#source-F5) |
| 6. **Smarters Pro** | Android/Android TV, iPhone/iPad/Apple TV, Samsung and web; Windows/macOS advertised as beta. Official site labels LG as coming soon—do not count it as launched. | Free/basic plus paid options; store/edition determines exact price. | Multiple local profiles are not upstream identities. No verified right to split your provider account. [F3](#source-F3) |
| 7. **iMPlayer** | Android mobile/TV and Apple mobile/TV advertised; centrally managed playlists, settings and device groups. Closest management-oriented candidate in this shortlist. | Listed from **$20/year or $35 lifetime**, starting with five devices; extra-device terms apply. Trial is not permanent free use. | **Best candidate for device configuration**, but provider-side accounts must still be independent for reliable customer revocation. [F2](#source-F2) |
| 8. **TiviMate** | Android TV/Google TV-oriented IPTV client; Fire TV requires an appropriate installation route. Not an iPhone/Apple TV/Roku app. | Limited free player; Premium paid. Live checkout price not reliably extracted. | Strong TV viewing candidate, not a provider-account or reseller-management system. [F4](#source-F4) |
| 9. **SmartOne IPTV** | IPTV player for supported Samsung, LG, VIDAA, Android/Google TV/Fire TV and additional TV systems. Exact model/region matters. | Paid activation; exact current checkout price not confirmed. | Device/playlist management documented; it does not independently revoke a shared provider secret. Good TV-specific candidate. [F11](#source-F11)[F12](#source-F12) |
| 10. **IBO Player** | Device-activated IPTV player; vendor material confirms Samsung/LG/Android/iOS families. Additional branded editions must be separately checked. | Vendor page lists **€10 one-time per device**; check exact app identity and activation portal. | Per-app device activation, not a substitute for independent upstream entitlements. Similar names and unrelated clones are a risk. [F13](#source-F13)[F14](#source-F14) |

### External-path decision

**Free-first choice:** IPTVnator on desktop, Kodi where its installation and TV interface suit the device, or SS IPTV on a specifically supported TV. Use VLC as a troubleshooting reference rather than your customer-management solution.

**Managed-device choice:** pilot **iMPlayer** on your actual device families and pair it with five genuine upstream identities. **TV experience choice:** TiviMate on Android TV when customer provisioning is handled elsewhere. **Broad mixed-device candidate:** Smarters Pro, accepting that beta and coming-soon labels are not production parity. [F2](#source-F2)[F3](#source-F3)[F4](#source-F4)[F6](#source-F6)[F7](#source-F7)[F9](#source-F9)

**Why this order:** changing players is inexpensive compared with committing to a provider whose entitlements cannot be managed safely. Ignoring that distinction can leave you unable to remove one customer's access without disrupting the others. An app upgrade also cannot repair an overloaded or unreliable upstream server.

### External-server systems that are a different category

| External system | What you receive | Your independent control | Fit |
|---|---|---|---|
| Authorized **Jellyfin** server invitation | URL and server-local account; app access to permitted libraries | Host administrator can create/disable separate users; as a viewer you cannot normally administer others | Best genuinely free server software path when the host cooperates; hosting/content are not automatically free. [J1](#source-J1)[J4](#source-J4) |
| Authorized **Emby** server account | Server identity and library permissions | Administrator controls users; feature/device entitlement may involve Premiere | Good alternative when the host operates Emby. [E1](#source-E1)[E2](#source-E2) |
| **Plex** library invitation | Plex account invitation to a personal server | Owner can remove individual shares; viewer is not the server administrator | Broad client ecosystem; remote-video payment rules apply. Plex's terms restrict personal-server access to permitted noncommercial use; do not treat paid access resale as approved. [P1](#source-P1)[P4](#source-P4) |
| Licensed provider's own service/app | Subscription and service-managed catalog | Usually household/account controls only; reseller control needs a separate agreement | Lowest server-maintenance burden. No file ownership or guaranteed third-party-player support. |
| Managed hosting of **your** media server | Rented server, bandwidth and storage; no content rights by default | You administer the server or contract with a managed operator | No home NAS needed, but storage, egress, backups and support still cost money. Obtain an all-in quote; a cheap virtual server is not a 200 TB media service. |

## 4. Twenty ways media reaches the system

**Key:** **FILE** means a usable local file, subject to its license—not ownership of copyright. **ACCESS** means streaming or app-controlled access. Every dollar range below is a budget allowance except the explicitly listed HDHomeRun prices. Source and platform availability were checked where documented; individual titles, regions and permissions still vary.

| Method / output | Equipment and software | Basic flow into your system | Cost and practical limits |
|---|---|---|---|
| 1. **DVD — FILE or disc playback** | DVD drive; compatible playback/copy tool; HandBrake for allowed conversion | Owned/authorized unprotected source → copy/convert → intake → NAS library | Drive allowance $25–60; discs extra. Commercial discs may be encrypted. Ownership alone does not establish permission to bypass DRM. [A1](#source-A1)[A15](#source-A15)[A16](#source-A16) |
| 2. **Blu-ray / UHD Blu-ray — FILE or disc playback** | Compatible Blu-ray/UHD drive and licensed playback; appropriate authorized extraction workflow | Allowed source → large MKV/video file → verify audio/subtitles → NAS; optional smaller viewing copy | Drive allowance $80–200+; UHD compatibility is not automatic. Large files, region/DRM constraints; no circumvention tutorial included. [A1](#source-A1)[A2](#source-A2) |
| 3. **Antenna TV tuner/DVR — FILE** | Antenna + HDHomeRun + recording storage; HDHomeRun, Jellyfin or Plex DVR as supported | Antenna → network tuner → DVR recording → named recording library → player | FLEX DUO **$109.99**, QUATRO **$149.99**, FLEX 4K **$199.99** listed; antenna ~$30–80 allowance. Current vendor DVR basic recording/playback is free; extended guide/advanced series $35/year. ATSC 3.0 DRM channels may not work. [A3](#source-A3)[A4](#source-A4) |
| 4. **Your phone/camera videos — FILE** | Existing phone/camera, USB/card reader; transfer/import software | Copy original → verify duration/checksum → home-video folder → backup → server | Usually $0 incremental; $10–40 cable/reader allowance. Preserve original before editing. Some HDR/HEVC files need a better client or transcode. [A2](#source-A2) |
| 5. **VHS/Hi8/analog home recordings — FILE** | Working original player, capture interface, computer and recording software | Tape playback in real time → capture file → cleanup/encode → home-video library | Capture kit allowance $30–150; working deck/service extra. A two-hour tape takes at least two hours to capture; damaged tapes need specialist care. [A2](#source-A2) |
| 6. **Internet Archive rights-cleared downloads — FILE** | Browser; no special hardware | Check item rights/download options → download original/derivative → intake and source record | Often $0. Not everything hosted is public domain or available for every reuse; avoid assuming upload equals authorization. [A5](#source-A5) |
| 7. **Library of Congress public-domain films — FILE** | Browser and ordinary download storage | Open the curated public-domain film selection → permitted download → classic-film library | $0. Historical selection, not a current commercial movie subscription. Review the specific item's rights statement. [A6](#source-A6) |
| 8. **NASA media library — FILE** | Browser; media download tools supplied by NASA | Select downloadable footage → preserve source/credit → educational library | Usually $0. Third-party copyrighted material, logos and identifiable people can impose additional limits; no implied NASA endorsement. [A7](#source-A7) |
| 9. **Bandcamp purchases — FILE** | Browser/account; music player/server | Buy or authorized free download → FLAC/MP3/etc. → music library → metadata scan | Artist-priced; allow $0–20+ per album. Actual files differ from the app's offline cache. Personal purchase does not grant resale/broadcast rights. [A8](#source-A8) |
| 10. **Qobuz download-store purchases — FILE** | Store account/browser/download manager | Buy a download → select delivered audio format → music folder → server | Title-priced; allow $10–30+ per album. Download-store purchase is distinct from a streaming subscription. [A9](#source-A9) |
| 11. **Rights-holder directly delivers a film/course — FILE** | Browser or secure file-transfer link; written download license | Creator-authorized MP4/MKV delivery → receipt/license saved → intake → library | Contract/title-specific; allow $0–100+ rather than assuming a universal fee. Confirm the purchase includes an actual file, not only a player login. |
| 12. **Podcast publisher download/RSS enclosure — FILE** | Podcast app or Audiobookshelf with RSS access | Publisher feed → permitted episode download → podcast/audio library | Usually $0 for public feeds; premium feed costs vary. Feed credentials are private; redistribution is not implied. [T12](#source-T12) |
| 13. **Your computer's screen/game/webinar recording — FILE** | Screen recorder or capture software and adequate local disk | Record content you control/have permission to record → MP4/MKV → intake | Often $0 software; optional capture hardware $30–200 allowance. Recording permission and participant privacy still apply. This is not a DRM workaround. [A2](#source-A2) |
| 14. **Existing authorized files on USB/another computer — FILE** | USB disk or SMB/NFS network share; copy/checksum utility | Copy or mount existing files → verify → organize → server | $0 incremental if equipment exists; any new storage extra. Duplicate detection should use content hashes, not just equal filenames. |
| 15. **Family/creator shares their own original files — FILE** | Authorized cloud download or local transfer | Permission confirmed → original downloaded → family/shared collection with access limits | Usually $0 incremental within existing transfer allowance. Receiving a file does not automatically transfer its copyright or privacy permissions. |
| 16. **Tubi / licensed free ad-supported services — ACCESS** | Supported television/phone/web app and internet | Service app → provider stream → screen; no NAS ingestion | Tubi free with ads. Catalog and geography vary. Not a source of unrestricted movie files for your own server. [A11](#source-A11)[A12](#source-A12) |
| 17. **Netflix and comparable paid streaming — ACCESS** | Supported app/device and paid plan | Subscription → service stream or permitted app download → service player | Allow ~$10–30+ per service/month; confirm checkout. Offline downloads expire and remain app-controlled, not NAS-ready files. [A10](#source-A10) |
| 18. **Authorized Jellyfin/Emby/Plex invitation — ACCESS, optionally FILE** | Matching app, server address/account/invitation | Remote server → authorized library → client; download only if host and rights permit | Player/server feature costs vary; see module 9. Host availability, bandwidth and library policy control access. [J1](#source-J1)[E1](#source-E1)[P1](#source-P1) |
| 19. **Licensed IPTV/operator playlist or portal — ACCESS** | Provider-issued endpoint/credentials and compatible player | Account → playlist/EPG + live/VOD stream → TV/phone | Provider quote plus any player activation. Concurrency, device binding, DVR and catch-up are separate entitlements. No automatic ownership or sublicensing. [F1](#source-F1)[F2](#source-F2)[F9](#source-F9) |


### 4A. Torrent sources and Sonarr/Radarr: added research

**What “good” means here:** useful catalog fit, a maintained integration, understandable access requirements, predictable file quality, and acceptable operational risk. Popularity alone does not establish safety, lawful availability or reliability. No copyrighted title was acquired, no private tracker account was opened, and no live credentialed download was tested. The source-code checks below verify that maintained Prowlarr definitions exist—not that every search, download or jurisdiction works today.

This is a **twentieth acquisition route: authorized BitTorrent downloads → FILE**, alongside the nineteen methods above. BitTorrent is the transfer method, a torrent indexer helps discover releases, and a tracker/peer network helps peers connect. They are not three names for Sonarr. Owning a disc or paying for a VPN does not automatically authorize downloading another person's upload. Apply the same rights check to public and private sources. Internet Archive also requires item-by-item review. [D1](#source-D1)[D2](#source-D2)

**The selected software chain:** approved source/indexer → **Prowlarr** manages compatible indexers → **Sonarr** chooses approved TV releases / **Radarr** chooses approved movies → **qBittorrent** transfers and, when permitted, seeds → intake verification → hard-link or copy into final media folders → Jellyfin/Plex scans the library. Sonarr/Radarr and Prowlarr are available from their own official project sites; you do not need a torrent site to download these apps. [T1](#source-T1)[T2](#source-T2)[T5](#source-T5)[D2](#source-D2)

| Source / research link | Best fit and access | Sonarr/Radarr integration evidence | Cost, workflow and practical judgment |
|---|---|---|---|
| **Internet Archive** — [torrent help and access](https://help.archive.org/help/archive-bittorrents/) | Rights-cleared/public-domain/creator-authorized material where the item actually permits it; public access | Direct item torrent into qBittorrent; **not verified as a general automated Sonarr/Radarr catalog** | Usually free. Review item rights → torrent → file → manual review/import. Best starting point for a clearly authorized transfer test; uneven seeding and item availability. [D1](#source-D1) |
| **1337x** — [primary hostname in maintained definition](https://1337x.to/) | Public general catalog; TV, movies and other categories | Prowlarr definition includes TV and movie search | Free access; qBittorrent + Prowlarr + TV/movie organizer. A reasonable general-source candidate **only for authorized material**, not a safety-certified default. The definition itself documents intermittent download-link and high-load search failures. Avoid random mirror lists. [D4](#source-D4) |
| **Nyaa.si** — [primary site](https://nyaa.si/) | Specialist East Asian/anime catalog rather than a general all-movie replacement | Maintained definition includes TV/movie modes and Sonarr/Radarr-specific matching options | Free access. Useful specialist candidate where rights permit; check episode numbering, language, subtitles, version and codec. A result being “anime” does not mean it is freely licensed. [D5](#source-D5) |
| **TorrentLeech** — [primary site](https://www.torrentleech.org/) | Private general tracker; lawful membership/admission required | Maintained Prowlarr definition supports authenticated TV/movie categories | Conditional candidate, **not the free-first default**. Membership terms, any fee, ratio and minimum seeding vary; current account rules are authoritative. Requires ongoing storage/upload for seeding. No invitation or membership was obtained, and private status is not a copyright license. [D6](#source-D6) |
| **EZTV** — [current primary hostname in definition](https://eztvx.to/) | Public **TV-focused** source | Maintained Prowlarr TV-search definition; Sonarr fit, **not a general Radarr movie source** | Free access. Narrow TV fallback where material is authorized. Challenge pages and episode/season naming may interrupt automation; existence of a TV search mode does not prove every season pack is available. [D7](#source-D7) |
| **YTS** — [current primary hostname in definition](https://yts.gg/) | Public **movie-focused, small-file HD** catalog | Maintained Prowlarr movie-search definition; Radarr fit, **not a Sonarr TV source** | Free access. Conditional compact-file candidate, not my default for archival-quality originals. Review bitrate, audio and subtitles; small size is a tradeoff, not proof of best image quality. API/domain changes can break integrations. [D8](#source-D8) |

**My recommendation is a small, tested source set—not every site at once.** Start with a rights-cleared file, qBittorrent and manual verification. Add Prowlarr and the relevant organizer only after paths, import and playback pass. For a continuing authorized collection, evaluate a general source plus a relevant specialist source; add a private tracker only when admission, content rights and seeding obligations make sense. The five catalog definitions above establish technical relevance to the requested automation tools, not a guarantee of licensed titles or uninterrupted operation.

#### What the Reddit sample actually says

I reviewed discussions in **r/selfhosted, r/sonarr, r/radarr, r/torrents and historical r/prowlarr**. This is not a statistically representative survey; I cannot honestly convert these threads into “most Reddit users agree.” Cached pages often expose relative ages rather than an exact publication date, so the source register records the **October 7, 2026 review date** and the displayed age instead of inventing a date.

| Community evidence | Opinion or reported issue | Decision for this design |
|---|---|---|
| **r/torrents: client crashes**; reviewed October 7, 2026 [U7](#source-U7) | Several respondents recommend qBittorrent; the original poster reports switching. | Use the official free qBittorrent client. This does not prove every competing client is unsafe. |
| **r/selfhosted: where to find indexers**; reviewed October 7, 2026 [U5](#source-U5) | Several commenters favor Usenet indexers such as NZBgeek, altHUB or DrunkenSlug; others report torrents meeting their needs, including 1337x. | Present both approaches. More paid sources are not automatically necessary; catalog fit and quality settings matter. These named Usenet services are community mentions, not independently tested purchase recommendations. |
| **r/sonarr: indexers**; reviewed October 7, 2026 [U6](#source-U6) | Questions mix up Usenet providers, indexers and torrent sites. | Label every component by job; never describe an indexer subscription as a complete download service. |
| **r/radarr: cleanup**; reviewed October 7, 2026 [U8](#source-U8) | Removing a library entry can leave a seeding copy/link in place; commenters suggest cleanup automation. | Use one explicit retention policy. Verify both library and download-client state before deleting; do not deploy another cleanup bot blindly. |
| **r/radarr: same title and year**; reviewed October 7, 2026 [U9](#source-U9) | A user reports an incorrect movie selection despite a similar title/year. The thread does not establish one universal cause. | Verify identity, audio/subtitles and a playback sample before automatic acceptance. A successful transfer is not a correct-content test. |
| **r/prowlarr: cartoon sources**; **June 3, 2023** [U10](#source-U10) | Historical recommendations mention private trackers and remind readers that RARBG had closed. | Use it to identify research questions, not to claim 2023 recommendations or mirror links are current. |

**Outdated-list warning:** the original **RARBG** is not a current recommendation. Its shutdown appears in the historical discussion; sites using that name are not proof the original returned. **TorrentGalaxy** had a prolonged outage and stopped upload bots reported in March 2025. I did not verify a genuine, dependable October 2026 continuation, so I do not select it as a reliable default. This is an explicit verification gap—not a claim that every similarly named site is necessarily fraudulent. [U10](#source-U10)[D10](#source-D10)

#### Usenet is an alternative, not another torrent website

The parallel flow is **authorized Usenet indexer result → Sonarr/Radarr → SABnzbd → paid Usenet provider → verified file → library**. The indexer finds an NZB reference; the provider supplies article access; SABnzbd downloads and assembles. Unlike a torrent peer, the usual downloader does not seed the completed file back to a swarm. Provider retention, completeness and removed articles can still cause failures. The cited Reddit users' preferences are opinions, not availability guarantees. [D9](#source-D9)[U5](#source-U5)[U6](#source-U6)

For budgeting only, reserve roughly **$5–15/month for a provider and $10–30/year per paid indexer**, then obtain current quotes; bundles, promotions and tiers can differ substantially. These are allowances, not verified checkout prices. Don't add recurring fees until you have a specific authorized collection and a demonstrated reason the free/manual route is insufficient.

#### Where this works in the two main approaches

**Your NAS/PC, or a rented server you administer:** the automation stack can run where you have authorized software installation and file-write access. A rented server may store everything off-site, so **this does not require a home NAS**. Account for remote storage, transfer quotas, seeding rules and whether the rental permits BitTorrent. These are provider-specific purchase gates, not assumed included features.

**Someone else's read-only Plex/Jellyfin library or IPTV subscription:** you normally cannot install Sonarr/Radarr there, change its sources or import files into its catalog. A host-operated request system may accept requests, but the host retains acquisition and rights responsibility. None of these tools subdivides your existing five-connection IPTV account into five independent customer credentials.

**Safety and reliability controls selected for the workflow:** download applications only from their official projects or verified stores; treat unexpected executables and “install a codec / paste a verification command” prompts as a stop condition. Keep download and organizer administration private, not exposed publicly. Bind the torrent client's network interface to the intended PIA interface when that is the chosen route; verify it fails closed using an authorized test transfer rather than assuming a VPN icon is enough. Keep local media serving outside that tunnel. qBittorrent documents explicit interface selection; the actual interface names and disconnect behavior must be tested on your host. [D2](#source-D2)[D3](#source-D3)[V1](#source-V1)

Place completed downloads and the final library on the **same filesystem** when using hard links, with consistent paths visible to all relevant applications. Hard links do not join separate NAS units; cross-filesystem imports copy data. A library deletion may leave a seeding link, so the disk space is not necessarily freed. Retain enough working space for temporary files, failed jobs, upgrades and seeding; pause intensive acquisition during fragile expansion/recovery. Do not defeat a private tracker's obligations with automatic cleanup. [T1](#source-T1)[T2](#source-T2)[U8](#source-U8)

**Torrent acceptance test:** one clearly authorized sample → correct indexer/category → successful transfer → verified title/file type/audio/subtitles → correct import → client playback → documented seed/retention behavior → VPN disconnect test where applicable. No automatic mass download is approved merely because this research package lists a source.

### A current example of why “buy” does not always mean permanent access

**Do not plan new purchases through Vimeo On Demand.** Its official notice says new purchases stopped **September 21, 2026**, and the service closes **November 20, 2026**. Existing purchases with seller-enabled downloads can be saved through the offered download function before access ends. This legacy recovery route is deliberately **not counted** among the nineteen acquisition methods in the table and the twentieth torrent route in section 4A. [A13](#source-A13)[A14](#source-A14)

### Ownership, law and recording boundaries

Keep source, purchase/license evidence, attribution and permitted audience with each valuable collection. This is especially important for customer-facing use. U.S. anti-circumvention rules are a separate question from owning a disc; applicable exemptions are limited, not a blanket “I bought it, therefore every copy is lawful” rule. A personal-media server license also does not grant commercial distribution rights. [A15](#source-A15)[A16](#source-A16)[P4](#source-P4)

HandBrake is an encoder, not a DRM-removal product; MakeMKV is a distinct disc tool and its existence does not settle the legal question. Use authorized/unprotected inputs or a properly licensed workflow. For OTA, verify your real channels and reception before selecting a tuner. FLEX 4K's name does not promise all local programs are 4K or that encrypted ATSC 3.0 works in Plex/Jellyfin. [A1](#source-A1)[A4](#source-A4)

## 5. NAS requirements explained

### First choose the role, then buy the box

| Architecture | Strength | Cost / maintenance | Recommendation for you |
|---|---|---|---|
| **No local server** | Zero disk-array administration; external provider handles storage and delivery | Existing device + player/license + authorized content plan | First choice while solving external account management. |
| **Existing computer** | Lowest incremental hardware cost; may already have Intel graphics | $0 hardware baseline; disk/NIC upgrades and electricity extra. Sleep, reboots and personal work interrupt service. CPU, GPU, drive bays and network are currently unverified. | Reuse only after inventory and testing. Do not erase or convert your working computer as an assumption. |
| **Dedicated PC/server with storage** | Flexible 10–12+ drive chassis, GPU/NIC slots, choice of Unraid or TrueNAS | Planning allowance $900–2,000 diskless before unusual GPU/rack needs; more hardware/OS administration | Best alternative when drive-by-drive flexibility matters more than appliance simplicity. |
| **NAS serves and stores** | One appliance to update; easy file management | NAS, drives, network and backup costs; graphics absent on many large models | Good for predominantly direct play. Choose verified GPU-capable hardware for difficult transcoding. |
| **NAS + separate media computer** | Storage survives a media-host replacement; graphics can be upgraded independently | Adds ~$500–1,050 for suitable computer + 10Gb NIC allowance; two systems to patch | **Preferred owned-media design**, particularly for mixed remote viewers and future second NAS. |

### Must-haves and optional upgrades

| Requirement | Priority | What it does and why it matters | Risk if omitted |
|---|---|---|---|
| **Ten actual 3.5-inch HDD bays** | Must for the specified NAS | Allows staged disk growth in one chassis. M.2 and 2.5-inch-only slots are not extra large-HDD bays. | An advertised “10/12/16-bay” model may reach far less bulk capacity than expected. |
| **10GbE end-to-end storage backbone** | Must | NAS, serving computer and switch/uplink all support 10GbE; clients may remain 1Gb/Wi-Fi. | A single 1Gb link caps transfers even with expensive disks and a 10Gb NAS port. |
| **Documented nondestructive RAID expansion** | Must | Supports adding drives without restoring the entire existing library. | Some pool layouts require a new group or migration; “ZFS” alone does not establish the answer. [R2](#source-R2)[R3](#source-R3)[R8](#source-R8) |
| **Two-drive parity for the large main array** | Design must | RAID6/SHR2/RAIDZ2 or dual parity buys a second disk-failure margin. Start four disks for conventional RAID6. | RAID5 is more exposed during lengthy rebuilds. Parity still does not protect against deletion, theft or ransomware. |
| **CMR drives, exact-model compatibility and supported firmware** | Must | Predictable sustained array writes; drive and NAS behavior tested together | SMR/unsupported models can perform poorly or complicate support. Do not assume every 26/30/32 TB SKU is approved. [N12](#source-N12)[R6](#source-R6) |
| **UPS with tested safe shutdown** | Must | Gives the NAS and host a controlled response to power failure | Unclean interruption during writes/expansion increases recovery risk. |
| **Backups + restore test** | Must | Protects originals, configuration and credentials separately from RAID | A healthy redundant array can still lose all data through human error, malware or a failed chassis. |
| **Adequate CPU / supported graphics path** | Must if transcoding | Hardware video decode/encode and tone mapping reduce CPU load | More RAM or ten drive bays will not compensate for a missing video engine. [J3](#source-J3) |
| **16 GB RAM baseline; 32 GB for heavier services** | Recommended | Room for OS, catalog, scans and containers. Some large-volume limits require specific RAM upgrades. | Memory pressure and model-specific volume ceilings; more RAM does not create GPU capability. [J3](#source-J3)[N11](#source-N11) |
| **ECC memory** | Strong preference | Helps detect/correct certain memory faults; valuable in an always-on storage system | Non-ECC is not automatically unusable, but offers less protection from memory errors. |
| **SSD for server database, artwork and transcode workspace** | Strong preference | Keeps browsing responsive while HDDs hold bulk video | Slow catalog access and competition between metadata jobs and media reads. [J3](#source-J3) |
| **NVMe read cache / write cache** | Optional | May help specific workloads; separate app SSD is usually higher priority here | Unneeded cost. Write cache adds failure/UPS considerations; it does not universally accelerate sequential movies. |
| **Link aggregation, 25GbE, GPU card, rack/dual PSU** | Optional | Useful for specific aggregate traffic, compute or availability goals | More heat, compatibility work and cost. Two 10Gb links do not automatically double a single stream. |

### Capacity: raw, parity-usable and comfortable working space

The following calculations use equal **26 TB** drives, decimal TB and two parity drives. Actual filesystem metadata, snapshots and reserved space reduce the result. **TiB** is the binary unit many systems display; 1 TB ≈ 0.9095 TiB.

| Drives / RAID6 | Raw capacity | After two-drive parity, before filesystem overhead | Approx. TiB | With 20% operational headroom |
|---|---|---|---|---|
| 4 × 26 TB | 104 TB | 52 TB | 47.3 TiB | 41.6 TB |
| 6 × 26 TB | 156 TB | 104 TB | 94.6 TiB | 83.2 TB |
| 8 × 26 TB | 208 TB | 156 TB | 141.9 TiB | 124.8 TB |
| 10 × 26 TB | 260 TB | **208 TB** | **189.2 TiB** | **166.4 TB** |
| 12 × 26 TB alternative chassis | 312 TB | 260 TB | 236.5 TiB | 208 TB |

**The important correction:** ten 26 TB drives can exceed 200 decimal TB after parity, but do **not** provide 200 TB of comfortably usable working space after headroom. Ten 24 TB drives give 192 TB before overhead; ten 30 TB give 240 TB, or 192 TB with 20% headroom. Ten 32 TB would give 256 TB, or 204.8 TB with headroom—but that is capacity arithmetic, **not verified compatibility or a current purchase recommendation**.

Three 26 TB disks in RAID5 give 52 TB with one-disk fault tolerance. Four in RAID6 also give 52 TB but tolerate two disk failures. That is why the decided starting design uses **four**, not three. Ten disks in RAID10 provide 130 TB; failure tolerance depends on which mirrored members fail, not simply “five disks can fail.” All calculations are derived, not vendor guarantees.

### “Rebuilding” does not normally mean wiping everything

**Rebuild after failure:** reconstruct the missing disk's contents from surviving data/parity onto a replacement. **Expansion/reshape:** reorganize the array so it can use a newly added disk; this may rewrite substantial data/parity. **Rebalance:** redistribute data across devices; not every storage system does this automatically. **Fresh rebuild from scratch:** delete/recreate storage and restore all data. These are different operations.

A supported online expansion is normally the second operation, not the fourth. The newly added disk can be erased while existing members remain intact. The operation still places substantial load on the array, may temporarily reduce responsiveness, and is not a substitute for a backup. A brief stop/restart or maintenance window can be required depending on the system. [R1](#source-R1)[R2](#source-R2)[R3](#source-R3)[R6](#source-R6)[R8](#source-R8)

**Time illustration:** reading/writing 26 TB at a sustained 100 MB/s is about **72 hours** for one full pass; at 200 MB/s about **36 hours**. These are arithmetic lower-level examples, not a promised rebuild time. Real reshapes can take several days or longer under load, with parity work, retries and background rate limits. Plan around days rather than assuming minutes. Maintain power protection; do not pull disks or begin another expansion while the array is degraded.

### Expansion behavior by operating system

| System | Add a disk without erasing existing library? | Size / layout restrictions | Availability and caveat |
|---|---|---|---|
| **ASUSTOR ADM RAID5/6** | Supported RAID online expansion and migration paths; verify the selected layout in current ADM | New/replacement disk must meet the array's minimum size. A larger disk's extra space is not automatically useful in conventional equal-member RAID. | Background work; same NAS remains the storage authority. Exact model/firmware and filesystem limits apply. [R1](#source-R1) |
| **Synology DSM / SHR / RAID** | Supported add-drive expansion for eligible pools; not every RAID type | SHR has its own mixed-size rules. Conventional RAID generally requires suitable equal-or-larger disks; replacing all required members may be necessary before capacity increases. | Pool expansion and volume expansion are separate. 108/200 TB volume limits vary by model/RAM. [R2](#source-R2) |
| **QNAP QTS / QuTS hero** | Yes for supported layouts. QuTS hero gained single-disk expansion in **5.1**; old “ZFS can never do that” advice is outdated. | Current 5.3 docs limit a RAID5/6 group to 16 members; disk size/type constraints apply. New-group expansion has separate rules. | Capacity appears after the background job completes. Validate firmware before choosing a layout. [R3](#source-R3)[R4](#source-R4)[R5](#source-R5) |
| **Unraid main array** | Yes; assign new disk, clear as required, then format the new member | Each data disk must be no larger than the smallest parity disk. Larger capacities may require a parity upgrade first. | Brief array stop for assignment; background clearing can preserve access. Existing files are not automatically redistributed. One-disk file reads/parity-write behavior differs from striped RAID. [R6](#source-R6)[R7](#source-R7) |
| **TrueNAS 25.10 / RAIDZ expansion** | Yes for supported RAIDZ expansion, adding a member to the vdev | New disk size/layout must qualify. Parity level does not increase just because a disk is added. | Online, resumable expansion. Old blocks can retain the old data/parity ratio until rewritten, so results can differ from a freshly created equally wide vdev. [R8](#source-R8) |

**Mixed-drive conclusion:** Unraid most directly matches “buy one additional disk as needed,” but introduces a different performance/protection model and requires a suitable host. For a vendor appliance, equal-size CMR drives in RAID6 are easier to predict. SHR improves flexibility on eligible Synology models; it is not available on every Synology, including the DS3622xs+ comparison here. [R2](#source-R2)[R6](#source-R6)[R7](#source-R7)[N6](#source-N6)

## 6. Ten NAS models ranked by fit—not by bay-count marketing

**Only one clearly current exact ten-HDD-bay recommendation was verified: AS6810T.** AS6510T is a second exact-ten-bay design with conditional older-stock availability. The other eight are explicitly labeled **8- or 12-HDD alternatives**. This is not a list of ten products all satisfying your exact bay requirement. Several alternatives also require adding a compatible 10Gb card.

Ranking prioritizes: your bay/network requirement, staged expansion, a sensible large-library role, and cost. It does not imply a benchmark contest. **N/R** means a comparable measurement was not retrieved. Prices marked “allowance” and older-model inventory need a fresh quote before purchase.

| Rank / model | True HDD bays; network | CPU / graphics | Stock RAM → maximum | Diskless price / status |
|---|---|---|---|---|
| **1 ASUSTOR AS6810T** | **10**; 2×10Gb RJ45 + 2×5Gb | Ryzen Embedded V3C14; **no iGPU** | 16 GB ECC DDR5 → 64 GB | **$2,212.99 listed, in stock**. Exact-fit leader. [N1](#source-N1)[C1](#source-C1) |
| **2 QNAP TS-1655** | **12 HDD + 4 small SSD slots**; 2×2.5Gb; add 10Gb NIC | Atom C5125, 8 cores; no video GPU; QAT is not Quick Sync | 8 GB → 128 GB; ECC option | **$1,999 listed** + NIC allowance $150–350. Not ten HDD bays. [N4](#source-N4)[C2](#source-C2) |
| **3 Synology DS2422+** | **12**; 4×1Gb; add compatible 10Gb NIC | Ryzen V1500B; no iGPU | 4 GB ECC → 32 GB | **$1,999.99 listed** + NIC/RAM. Not ten bays. [N5](#source-N5)[C3](#source-C3) |
| **4 Synology DS3622xs+** | **12**; dual built-in 10Gb RJ45 | Xeon D-1531, 6 cores; no iGPU | 16 GB ECC → 48 GB | **$3,000–3,500 allowance**, current quote unverified. Not ten bays. [N6](#source-N6) |
| **5 QNAP TVS-AIh1688ATX** | **12 HDD + 4 small-drive slots**; dual 10Gb + dual 2.5Gb | Core Ultra 9 285; Intel graphics, new driver/firmware path | 48 GB ECC → 192 GB | **$5,199 listed**. Premium integrated-compute alternative, not ten HDD bays. [N7](#source-N7)[C4](#source-C4) |
| **6 QNAP TVS-h874-i5-32G** | **8**; 2×2.5Gb; add 10Gb NIC | Core i5-12400 / UHD 730 | 32 GB → 64 GB | **$2,200–2,700 allowance** + NIC. i9 edition differs; don't borrow its built-in card claim. [N8](#source-N8) |
| **7 ASUSTOR AS6510T** | **10**; dual 10Gb + dual 2.5Gb | Atom C3538; no iGPU | 8 GB → 64 GB | **$1,595 indexed marketplace offer**; older stock/warranty conditional. [N3](#source-N3)[C7](#source-C7) |
| **8 QNAP TS-1273AU-RP** | **12**, rack; dual 2.5Gb; add 10Gb NIC | Ryzen V1500B; no iGPU; optional GPU subject to constraints | 8 GB → 64 GB | **$2,599 listed**, lead-time/preorder wording; + NIC. [N9](#source-N9)[C5](#source-C5) |
| **9 QNAP TS-1232PXU-RP** | **12**, rack; dual **10Gb SFP+** + dual 2.5Gb | Annapurna Labs AL324 ARM; no suitable video GPU | 4 GB → 16 GB | **$1,749 listed**. Low-cost storage role, not a transcoding pick. [N10](#source-N10)[C6](#source-C6) |
| **10 Synology DS1825+** | **8**; dual 2.5Gb; optional 10/25Gb NIC | Ryzen V1500B; no iGPU | 8 GB ECC → 32 GB | **$1,200–1,400 allowance** + NIC/RAM. Does not meet ten-bay requirement. [N11](#source-N11) |

### Serving, expansion, capacity and operating burden

“Plex/container” below means an appropriate current NAS package or container route must be confirmed for that OS/CPU architecture; it does not mean the appliance has been test-installed here. On x86 models a separate Linux media host accessing SMB/NFS avoids NAS-app package lag entirely. Jellyfin hardware acceleration is free; Plex hardware acceleration requires the appropriate Plex Pass entitlement. [J3](#source-J3)[P1](#source-P1)

| Model | Media-server role / transcoding assessment | Growth and enclosure path | Full internal RAID6 math at 26 TB; power/noise/maintenance |
|---|---|---|---|
| **AS6810T** | x86 Plex/container route; excellent storage/direct-play role. **Do not buy for GPU 4K transcoding.** Use separate graphics-capable host. | ADM expansion; vendor maximum 22 HDDs using compatible four-bay expansions. External capacity is separate, not automatic extension of internal volume. | **208 TB before overhead**. Vendor operation ~68 W; published idle sound ~22 dB, not ten-drive seek noise. One ADM appliance plus media host to maintain. [N1](#source-N1)[R11](#source-R11) |
| **TS-1655** | x86 app/container platform; CPU-only video unless an explicitly supported GPU solution is added. Prefer separate host. | QTS/eligible QuTS hero expansion; compatible QNAP SATA/SAS/PCIe shelves require exact HBA/cable/model matrix. | **260 TB**. Vendor typical ~105 W under its test configuration. Fan/HDD noise; more NIC/OS/expansion choices to maintain. [N4](#source-N4)[R3](#source-R3)[R5](#source-R5) |
| **DS2422+** | Plex/Container Manager route; CPU-only for this processor. Separate host for demanding conversion. | SHR2/RAID6; **one DX1222 → 24 HDDs**. Prefer a separate pool on the enclosure. Check volume size and memory requirements. | **260 TB pool arithmetic**, not guaranteed single-volume size. Comparable populated power/noise N/R. DSM relatively straightforward; 4 GB stock is not the desired final RAM here. [N5](#source-N5)[R2](#source-R2) |
| **DS3622xs+** | Strong storage CPU, but Xeon name does not create Quick Sync. Plex/container or external server. | RAID6, **no SHR**; **two DX1222 → 36 HDDs**. Separate pools preferred; volume limits can require additional RAM/multiple volumes. | **260 TB** before overhead. Comparable populated power/noise N/R; premium chassis and larger power/cooling footprint. [N6](#source-N6)[R2](#source-R2) |
| **TVS-AIh1688ATX** | GPU exists, but **actual Plex/Jellyfin hardware encode/tone-map support is conditional on current driver/OS/container support**. Not a verified five-4K-stream claim. | QuTS hero; compatible QNAP shelves/HBAs. Four small-drive slots useful for system SSDs, not four additional 26 TB HDDs. | **260 TB** in 12 HDD slots. Published typical ~131 W, configuration-dependent. High initial spend; current-platform firmware validation needed. [N7](#source-N7)[C4](#source-C4) |
| **TVS-h874 i5** | UHD 730 makes this the strongest established integrated-transcoding candidate here; expose GPU correctly and verify codecs/subtitles. Plex Pass needed for Plex HWA. | Eligible QuTS hero expansion; compatible shelves. Internal eight-HDD limit misses your requirement. | **156 TB**. Published typical ~82 W; loaded HDDs/fans audible. One-box option at the cost of bay count. [N8](#source-N8)[J3](#source-J3)[P1](#source-P1) |
| **AS6510T** | Older x86 storage/direct-play platform; no iGPU. Separate media host strongly preferred. | ADM expansion; compatible AS6004U route, historically up to 18 HDDs total. Confirm present firmware and support status before buying. | **208 TB arithmetic**, but 26 TB HCL not validated here. Comparable populated sound/power N/R. Older-stock support risk. [N3](#source-N3) |
| **TS-1273AU-RP** | x86 apps/container route; external transcode host avoids optional-GPU clearance, power and PCIe conflicts. | QNAP rack expansion compatibility matrix; separate shelf/pool design. NIC may compete with optional GPU/HBA slot use. | **260 TB**. Vendor test ~79 W; small rack fans and redundant supplies favor an equipment room, not a bedroom. More hardware service complexity. [N9](#source-N9) |
| **TS-1232PXU-RP** | **Storage-first recommendation.** ARM package availability differs; a reliable current model-specific Jellyfin/Plex installation was not verified. External x86 server avoids this risk. | Supported QNAP expansion only, with exact matrix. SFP+ optics/DAC and a matching switch are required. | **260 TB arithmetic**. Comparable populated power/noise N/R; rack noise and architecture-specific packages are trade-offs. [N10](#source-N10) |
| **DS1825+** | Plex/Container Manager route, no iGPU; use separate media host. | SHR2/RAID6; **two DX525 → 18 HDDs**. USB-C-shaped expansion interface is not permission to use arbitrary USB enclosures. | **156 TB** internal. Vendor maximum single volume 200 TB with 32 GB RAM; 108 TB without qualifying upgrade. Comparable populated sound/power N/R. [N11](#source-N11) |

**Capacity caution for every row:** the 26 TB figures are a common comparison calculation, not a statement that every listed NAS approves every 26 TB disk. Obtain an exact drive-SKU/firmware compatibility confirmation. On models with a smaller maximum volume, use multiple supported volumes/folders within one media library rather than assuming a 260 TB single volume.

**Noise and power caution:** published watts use different disks and tests; they are not normalized ten-drive measurements. PSU wattage is a maximum supply rating, not your electric bill. Ten rotating drives will produce seek noise even in a quiet chassis. Put the NAS on a ventilated stable shelf away from the TV microphone/bedroom; avoid an unventilated cupboard. At an assumed $0.30/kWh, a measured 100 W average is about $263/year; 200 W is about $526/year. Use your actual rate and a wall meter before treating these as operating costs.

### Initial and growth costs across the shortlist

To compare fairly, the same illustrative four-drive set is used: **4 × $1,144.99 = $4,579.96**, based on the retrieved 26 TB retail listing. This is not an approved drive order. Add ~$710–1,200 shared allowance for switch, UPS, cabling and protected configuration storage; add ~$500–1,050 for a separate 10Gb-connected transcoding host where recommended. Tax, installation labor, content plans, RAM upgrades and a full media backup are extra. [C8](#source-C8)

| NAS | NAS + required 10Gb card + four-drive comparison subtotal | Cost of filling remaining internal HDD bays at same illustrative drive price | Extra costs to expect |
|---|---|---|---|
| AS6810T | **$6,792.95** | Six more drives: **$6,869.94** | Separate host; common network/UPS; optional RAM/SSD. |
| TS-1655 | ~$6,729–6,929 | Eight more: **$9,159.92** | Host; compatible NIC; RAM; optional mirrored system SSD pool for QuTS hero. |
| DS2422+ | ~$6,730–6,930 | Eight more: **$9,159.92** | Host; NIC; substantial RAM upgrade; volume planning. |
| DS3622xs+ | ~$7,580–8,080 | Eight more: **$9,159.92** | Host; RAM if needed; premium enclosure expansion. |
| TVS-AIh1688ATX | **~$9,779** | Eight more: **$9,159.92** | Mirrored system SSDs; app/GPU validation; host only if integrated path fails requirements. |
| TVS-h874 i5 | ~$6,930–7,630 | Four more: **$4,579.96** | NIC; system SSDs; earlier enclosure/second-NAS need. |
| AS6510T | **~$6,175**, conditional old-stock offer | Six more: **$6,869.94** | Host; possible support/firmware limitations; exact drives must qualify. |
| TS-1273AU-RP | ~$7,329–7,529 | Eight more: **$9,159.92** | Rack/rails, host, NIC and potentially specialized shelf/HBA. |
| TS-1232PXU-RP | **~$6,329** | Eight more: **$9,159.92** | External host; SFP+ networking; rack/rails. |
| DS1825+ | ~$5,930–6,330 | Four more: **$4,579.96** | Host; NIC; RAM; expansion arrives sooner because only eight HDDs. |

These deliberately large current drive allowances prevent an outdated $400-per-disk sale from becoming your purchase budget. A fresh multi-vendor quote may change the preferred drive size or favor a 12-bay alternative. Another retrieved retailer listed the same capacity at $1,240.99 and out of stock; a third at $1,312.99. Price and availability are material uncertainties, not rounding errors. [C8](#source-C8)[C9](#source-C9)[C10](#source-C10)

## 7. Growth beyond one NAS: one library is not one storage pool

| Growth method | Connection and compatibility | What becomes unified | Failure behavior / limits | Cost and complexity |
|---|---|---|---|---|
| **Second standalone NAS** | Both units → 10Gb switch; server mounts separate SMB/NFS shares. Brands can differ. | One Jellyfin/Plex library can index folders from both; users see one catalog. Storage remains two pools and two admin systems. | Failed NAS takes its own files offline; the other can keep serving. The shared media computer remains a single service dependency. | Another chassis + drives + UPS capacity/network port. **Recommended default** for continued growth. |
| **Vendor expansion enclosure** | Model-approved USB, SAS, SATA or PCIe connection; not generic “plug any NAS into any NAS.” | One host administers additional disks; whether a pool can span depends on vendor/layout. | Host failure affects its enclosures. Cable/enclosure loss can take a spanned pool offline. Enclosure has no independent NAS CPU/network identity. | Four-bay USB allowance ~$350–600; large shelves ~$1,000–2,500+ plus disks/HBA/cables, model-specific quote required. Lower chassis cost, greater host dependency. |
| **One media application, multiple folders** | Stable shares mounted on one media host; identical paths survive reboot | **Viewing experience** and user library permissions | Unavailable share affects corresponding media; turn off destructive cleanup/empty-trash-on-missing-storage behavior until mounts are healthy. | Usually no extra storage software license; small setup/admin burden. This is the chosen unification layer. |
| **mergerfs-style combined namespace** | Linux combines directories, including mounted shares; storage filesystems remain separate | One path such as `/media`, not a new protected distributed filesystem | No automatic parity/replication/rebalancing. Files on failed branches unavailable; duplicate-name and write-placement policies matter. | Free software, added mount/permissions/troubleshooting work. Optional—not required for one movie library. [R9](#source-R9) |
| **Distributed clustered storage** | Multiple nodes, adequate network, supported failure domains/quorum and replication design | Genuine cluster-level storage namespace and management features | Node redundancy depends on replica/erasure layout and quorum; two arbitrary NAS boxes are not automatically a fault-tolerant cluster. | Highest complexity and capacity overhead. Not the simple starter path for this media use. |

### Specific enclosure realities

**ASUSTOR:** AS6004U is a four-bay USB 3.2 Gen1 device—**5Gb/s link**, not 10GbE. AS6810T's advertised maximum is 22 HDDs with compatible expansions. Treat the external capacity as separate supported storage rather than assuming the ten-disk internal volume expands across it. USB bandwidth, host dependency, cable stability and enclosure support remain limits even though the NAS has fast Ethernet. [N1](#source-N1)[R10](#source-R10)[R11](#source-R11)

**Synology:** DS2422+ supports one DX1222; DS3622xs+ two DX1222; DS1825+ two DX525. These are specific supported pairings. Use a separate pool per chassis where practical so one enclosure link is not a dependency of an enormous spanned volume. “Maximum disks connected” is not the same as “maximum protected single volume.” [N5](#source-N5)[N6](#source-N6)[N11](#source-N11)

**QNAP:** expansion can require a specific shelf, HBA and cable; USB, SATA/SAS and PCIe shelves are not interchangeable. The retrieved QuTS hero documentation warns that a disconnected enclosure can make a pool containing its RAID group inaccessible, and one RAID group cannot arbitrarily mix disks across enclosures. Do not buy a shelf based only on the QNAP logo. The exact shelf-count ceiling for each ranked model was not independently verified; obtain the manufacturer's compatibility result before purchase. [R5](#source-R5)

### The decided expansion path

**Start:** four equal approved disks in RAID6, shared folders and one serving computer. **Within chassis:** add same-size approved disks one at a time, after healthy-array and backup checks. Verify the completed expansion and actual pool/volume capacity before adding another. **At around 70–80% working occupancy or when further additions no longer meet the growth target:** commission a second NAS with its own protected pool. Mount it on the same serving computer and add its folders to the existing library.

Maintain separate monitoring for each NAS and a single documented inventory: unit, pool, volume, share, library, free space, parity state, backup state and last restore test. This gives **one viewing system and one operating checklist**, not one magical vendor dashboard. Further NAS units repeat the same pattern; enough switch ports and host network throughput must remain available.

## 8. The actual starting configuration and ten-gigabit network

### Owned-media configuration selected for this design

**Storage:** ASUSTOR AS6810T; start with four equal-capacity **approved CMR** disks, preferably 26 TB if the exact SKU/firmware is supported; RAID6; stock 16 GB ECC initially. The 26 TB compatibility confirmation is an explicit purchasing gate. A 24 TB fallback starts at 48 TB after parity and reaches 192 TB at ten disks before overhead. No particular disk is declared approved just because another ASUSTOR family lists it. [N1](#source-N1)[N12](#source-N12)

**Serving computer:** Intel Core i5 with usable integrated graphics, preferably 12th generation or newer; **not an F-series model without graphics**; 16–32 GB RAM; 500 GB–1 TB SSD for OS, database/artwork and temporary transcodes; compatible 10Gb NIC. Linux plus maintained Jellyfin/Plex software is the default serving design. Existing equipment can replace this purchase only after its capabilities are checked. The exact OS/driver/software combination must pass the real media tests below. [J3](#source-J3)

**Software:** Jellyfin is the free-first server choice. Add Plex only where its client experience materially helps, with its current paid-feature rules accepted. One server is the default source of watched-state/user administration; running both does not automatically synchronize their accounts or watched status. Keep media mounts read-only for the serving process where possible; give organizing tools only the write permissions they need.

**Network and safety:** 10Gb RJ45 switch path between NAS and host; Cat6a; router/firewall; existing suitable playback devices; UPS with shutdown integration; separate backup of originals and configuration. This is a specified architecture, not a hardware order or an installed service.

### Network parts and costs

| Part | Required function | Planning allowance / compatibility |
|---|---|---|
| NAS port/card | At least one real 10Gb link | Built into AS6810T; other models need compatible PCIe card ~$150–350. Check slot width, height, OS support and vendor list. |
| Serving computer NIC | 10Gb connection to storage | ~$100–250; RJ45 or SFP+ must match switch/cabling. Small mini PCs may lack PCIe; a compatible Thunderbolt/USB4 solution costs more and must be validated. |
| 10Gb switch | Enough ports for NAS1, host, future NAS2 and optionally workstation | ~$250–600 for a suitable small unit; fanless/managed/port types change cost. Router need not itself route internet at 10Gb for local switched storage traffic. |
| Cables / transceivers | Correct physical connection, not just matching connector appearance | Cat6a patch cables ~$10–30 each for RJ45. SFP+ DAC ~$15–40 where both ends support it; optical modules/fiber or RJ45 modules extra. DAC cannot plug into AS6810T's RJ45 port. |
| UPS | Runtime for safe shutdown of both storage and host | ~$200–400 allowance; size by measured watts and shutdown/runtime needs, not just VA advertising. |
| Backup/configuration media | Protected copy outside the primary pool | ~$100–200 initial allowance covers configuration and limited originals, **not a full 200 TB duplicate**. Larger backup needs a separate budget. |

**10GbE is 10 gigabits per second, not 10 gigabytes:** its raw ceiling is 1.25 GB/s before protocol overhead. An optimized link might transfer roughly 0.8–1.1 GB/s, but the HDD array, small files, encryption and other jobs may be slower. This is a design expectation, not a measured benchmark. Ordinary video streams use far less; 10Gb matters particularly for ingest, backups, many simultaneous jobs and multiple storage units.

**Internet upload is separate.** A 10Gb NAS will not make a 20 Mb/s home upload capable of delivering five 80 Mb/s movies. With an external provider, its upload and your download matter. With your server and remote viewers, **your upload** is the limiting direction.

| Five simultaneous streams: illustrative bitrate | Total media payload | Suggested upload target with operating headroom | Interpretation |
|---|---|---|---|
| 5 × 8 Mb/s, 1080p example | 40 Mb/s | About 60 Mb/s stable upload | Bitrate is a chosen profile, not a universal 1080p value. |
| 5 × 20 Mb/s, compressed 4K example | 100 Mb/s | About 140–150 Mb/s | Some sources need more; watch peaks and other household traffic. |
| 5 × 80 Mb/s, high-bitrate 4K example | 400 Mb/s | About 550–600 Mb/s | Remux peaks can be higher. Prefer direct play on a capable client, or create a smaller remote version. |

Numbers are arithmetic planning scenarios with roughly 30% headroom; simultaneous download/upload tests, ISP data limits and sustained evening performance are part of acceptance. A television with a 100Mb Ethernet port can itself be a bottleneck for high-bitrate 4K despite a fast NAS.

### What this starting system costs

At the retrieved $2,212.99 NAS and four × $1,144.99 illustrative drives, plus $500–1,050 host/NIC and $710–1,200 common network/UPS/configuration allowance, the complete starting **hardware allowance is about $8,003–9,043 before tax**. It excludes installation labor, a full second copy of the media, service subscriptions and additional RAM/system SSD choices. [C1](#source-C1)[C8](#source-C8)

Filling the last six bays adds **$6,869.94** at that same example drive price—not a forecast of the price when you expand. A second identical four-drive unit is roughly **$6,793** for NAS + disks at the same reference prices, plus incremental UPS/network capacity; the existing media host can serve both if testing shows sufficient capacity. External-only viewing avoids this entire NAS outlay.

## 9. Serving, playback and accounts across real platforms

### Server versus player versus account

**Server** stores/indexes media, checks permissions and may convert formats. **Player** runs on the TV/phone and decodes what it receives. **Account management** grants access; a device can have several local profiles without creating separate upstream customers. A NAS network share by itself is not a polished multiuser streaming service.

| Platform family | Plex | Jellyfin | Emby |
|---|---|---|---|
| Windows / macOS / Linux | Web and supported desktop apps | Web and Jellyfin Media Player | Web and supported desktop clients; consult current download entry for each OS |
| Android phones/tablets | App | App | App |
| iPhone / iPad | App | Jellyfin app; Swiftfin alternative | App |
| Android TV / Google TV / Fire TV | TV apps | Android TV / Fire TV apps | TV apps |
| Apple TV | App | **Swiftfin** listed as official/beta; third-party clients also exist | App |
| Roku | Channel/app | Official client | Channel/app |
| LG webOS | Supported models | Official client listed; model/OS/region constraints | Supported models |
| Samsung Tizen | Supported models | Current official client directory lists Tizen; confirm your model/store region, not older blanket “sideload only” advice | Supported models |
| Xbox | Supported app | Current directory lists Xbox client | Listed client |
| PlayStation | Plex lists PlayStation support; exact console generation matters | No equivalent native client verified in this research | Legacy/browser entries should not be confused with a current native app; not verified here |
| Web browser | Yes, subject to codec support | Yes, supported modern browsers | Yes, subject to codec support |

Platform inventory comes from current official directories, not estimated device counts. It verifies the existence of an application route, not identical features on every device. Casting is not treated as a native app. Check app generation, OS minimum, store country, subtitle handling, HDR format, audio passthrough and remote behavior for **your actual device** before selecting the server. [P2](#source-P2)[P3](#source-P3)[J1](#source-J1)[J2](#source-J2)[J4](#source-J4)[E1](#source-E1)

### Cost and administration

| System | Free use / paid features | Identity and remote access | Best fit |
|---|---|---|---|
| **Jellyfin** | Free/open-source server and official clients; hardware acceleration, users and DVR not paywalled. Third-party clients may charge. | Server-local users, permissions and administration. Secure remote connectivity must be operated; no included commercial hosting. | Best free-first owned server, or authorized external host with independent accounts. [J1](#source-J1)[J3](#source-J3)[J4](#source-J4) |
| **Plex** | Local personal-video use has a free path; hardware transcoding/DVR and other features need Plex Pass. Remote personal-video eligibility is separate. | Plex account and server sharing. Remote video works when the server administrator has Plex Pass, or the viewer has qualifying Plex Pass/Remote Watch Pass. | Broad consumer-device experience when paid rules and personal-use terms fit. [P1](#source-P1)[P4](#source-P4) |
| **Emby** | Free server tier; some apps/features require unlock or Premiere. Listed Premiere **$4.99/month, $54/year or $119 lifetime**. | Server users plus optional Emby Connect. Premiere terms describe a single-household allowance of 30 devices, **not 30 simultaneous streams or a reseller license**. | Middle option when Emby clients/features suit the household. [E1](#source-E1)[E2](#source-E2) |
| **Kodi / VLC / Infuse-type local client** | Varies; Kodi/VLC free, other clients can charge | Plays shares or connects to a server; not automatically a server-side user manager | Good direct-play endpoint, not a replacement for upstream account controls. [F7](#source-F7)[F8](#source-F8) |

**Plex price correction:** Remote Watch Pass regular pricing after **June 1, 2026** is **$2.99/month or $29.99/year**, rather than older $1.99/$19.99 figures. It does not itself give your server hardware transcoding. The current Plex Pass checkout amounts, particularly lifetime, were not reliably extracted; no older lifetime figure is presented as today's price. A Plex Pass held by the **server administrator** can satisfy remote-video access for viewers of that server. [P1](#source-P1)

### Direct play, remux and transcoding

**Direct play** sends the original video/audio/container for the client to decode; the server primarily reads and transfers. **Remux/direct stream** changes packaging, and sometimes audio, without necessarily re-encoding video. **Video transcode** decodes and re-encodes the image, often to reduce bitrate or make an unsupported codec usable. Hardware acceleration uses a supported video engine; a large general-purpose CPU, RAID card or “AI” label alone is not evidence of that capability. [J3](#source-J3)[J4](#source-J4)

A capable client may directly play 4K while an incompatible client forces conversion of a 1080p file. **Subtitles matter:** text subtitles are often easy; image subtitles or styled subtitles can require burn-in, making the server render them into the video. HDR-to-SDR tone mapping adds work. An unsupported audio format can sometimes be converted without touching video. The most efficient solution is often a better client or an appropriate alternate file, not a larger NAS. [J3](#source-J3)[J4](#source-J4)

### Five viewers: what is actually safe to promise?

For five direct-play 1080p streams, healthy storage and network throughput are normally more relevant than a powerful GPU. For five mixed 4K streams, no honest universal stream-count claim follows from a CPU name. Bitrate, codec, 10-bit/HDR, tone mapping, subtitle burn-in, audio and software version all change the workload. The AS6810T and most large-storage alternatives here lack integrated graphics; the separate Intel host is intended to absorb that variability, not to guarantee five worst-case conversions without testing. [J3](#source-J3)[N1](#source-N1)[N4](#source-N4)[N5](#source-N5)[N6](#source-N6)

The acceptance workload must include five real target-device sessions: ordinary 1080p, high-bitrate 4K direct play, HDR-to-SDR conversion, a subtitle-heavy title and a remote constrained-bandwidth stream. Confirm from server telemetry whether hardware acceleration is really in use. Test sustained playback and seeking, not just whether a movie starts. If the worst case exceeds capacity, use direct-play-compatible clients, limit simultaneous transcoding, prepare an alternate remote version or add proven graphics capacity.

### PIA compatibility and conflicts

PIA can coexist with these systems, but it is a **privacy VPN route**, not automatically a private mesh joining your televisions to your NAS. A full-tunnel VPN can change the apparent location/IP, block local discovery, interfere with LAN access through kill-switch rules, change return routing or break inbound reachability. Providers may restrict VPN use, shared-IP addresses or geographic access. [V1](#source-V1)[V2](#source-V2)

**Chosen layout:** keep NAS administration, local shares and the public-facing media server off a blanket PIA tunnel. Apply PIA only to the specific authorized application/container that needs it, using supported split tunneling/isolation. Permit required LAN access without weakening the firewall broadly. Where remote access is needed, use a properly secured HTTPS endpoint or an explicitly configured private-access VPN suited to the clients; do not expose the NAS administrator dashboard directly.

PIA port forwarding is location-dependent, not available on its US servers according to the retrieved guidance, and supplies an assigned port rather than an arbitrary permanent one. Router port forwarding at home does not automatically open the PIA exit or defeat ISP carrier-grade NAT. DDNS tracks a changing address; it does not create inbound reachability. Test remote access from a different internet connection, with the final VPN and firewall settings in place. [V1](#source-V1)[V2](#source-V2)

## 10. Supporting tools: useful, optional and correctly placed

The simplest system is **server + clean folders + backups**. Do not deploy every tool below just because it is commonly discussed. Sonarr and Radarr coordinate acquisition/organization; they do not grant content rights, manufacture provider accounts, or make a remote read-only library writable.

| Tool | Job and place in the flow | Your owned-media path | External-provider path |
|---|---|---|---|
| **Jellyfin/Plex/Emby metadata** | Scan final files, match titles, fetch artwork and present a catalog | Essential server function; manually correct bad matches before adding more automation | Host/provider does it. You may lack permission to change it. [J4](#source-J4)[P3](#source-P3)[E1](#source-E1) |
| **Sonarr** | Episode monitoring, quality rules, naming/import and integration with download clients | Optional. Needs library write access, supported sources/client and consistent paths. Do not assume it imports Netflix subscriptions. | Unnecessary for pure streaming; useful only if upstream grants a real managed storage/workflow role. [T1](#source-T1) |
| **Radarr** | Movie monitoring, quality rules, import/rename and download-client integration | Optional; same source/permissions considerations | Does not control provider catalogs or customer accounts. [T2](#source-T2) |
| **Bazarr** | Finds/manages subtitles alongside Sonarr/Radarr libraries | Optional; requires their integration, subtitle-provider access and file write permissions | Usually host-only; cannot attach files to an arbitrary remote provider library. [T3](#source-T3) |
| **qBittorrent / SABnzbd** | Actual torrent / Usenet transfer, respectively; different protocols | Optional download engine where approved sources need it. Verify paths, retention and network isolation. | Only on a host you administer with permission; irrelevant to ordinary read-only streaming. [D2](#source-D2)[D9](#source-D9) |
| **Prowlarr** | Central indexer management for compatible automation tools | Optional only where lawful indexed sources are part of the workflow; not a downloader itself | No role in ordinary provider playback. [T5](#source-T5) |
| **Seerr** | Requests and approval workflow with media-server and Sonarr/Radarr integration | Optional once several users request additions; require administrator approval and authorized sources | Only where the external host offers it; a request is not a guarantee of licensed acquisition. [T4](#source-T4) |
| **tinyMediaManager / naming tool** | Review title identity, NFO/artwork and filenames before ingestion | Optional; choose one authority for renaming to avoid tools fighting each other | No access to provider files means no useful write role. [T6](#source-T6) |
| **Tautulli** | Plex viewing/stream telemetry | Optional for understanding direct play, transcodes and usage; protect viewer privacy | Only the server administrator or delegated operator can deploy it usefully. [T7](#source-T7) |
| **Kometa** | Plex collections, overlays and catalog presentation automation | Optional cosmetic/curation layer after a stable library | Requires relevant Plex administrator/API access; not a universal IPTV catalog manager. [T8](#source-T8) |
| **HandBrake / Tdarr** | Prepare compatible or smaller files; Tdarr coordinates library processing | Optional. Preserve originals or backups; avoid simultaneous heavy encoding and RAID expansion | Not relevant without authorized file access. [A1](#source-A1)[T9](#source-T9) |
| **rclone / restic / NAS backup tools** | Transfer files and protect copies/configuration | Backup function essential; particular tool optional. Encryption, retention and restore verification matter. | Back up your account inventory/settings only; do not assume you may mirror the provider's entire library. [T10](#source-T10)[T11](#source-T11) |
| **Audiobookshelf** | Audiobook/podcast server and feed organization | Optional dedicated audio experience for authorized books and podcasts | Connect only to a host that offers it; not a video-provider replacement. [T12](#source-T12) |

**Path and permission design:** one intake location; separate Movies, TV, Music, Home Video and Recordings; stable mount names for NAS1 and NAS2; consistent paths visible to organizer and download client. Hard links do not span separate filesystems or NAS units. Cross-NAS moves therefore often copy data and take time. The media player gets read access; organizers get carefully scoped write access. Back up application databases and API settings before upgrades. [T1](#source-T1)[T2](#source-T2)

**Operational policy:** approve content/source changes; check new files before catalog inclusion; avoid competing rename tools; schedule intensive jobs away from viewing/expansion; monitor free space, array health and backup failures; test restoration periodically. External customers need a separate entitlement inventory because library metadata is not a billing/provisioning system.

## 11. Community evidence, uncertainty and acceptance

### What communities actually add

This is a small qualitative sample, not a statistical survey or proof that a tool is universally reliable. Technical conclusions are checked against official documentation; community comments supply failure patterns and practical questions.

| Dated community source | Reported experience / opinion | Design response |
|---|---|---|
| **Reddit r/homelab, May 19, 2025** | User wanted files on a NAS and Jellyfin on another host; replies proposed mounting SMB/NFS shares. | Supports the practicality of separating compute/storage, not a performance guarantee. Keep one library with stable mounts. [U1](#source-U1) |
| **Reddit r/selfhosted, April 3, 2026** | Reusing an older PC prompted reports of Quick Sync/BIOS/driver problems despite adequate general CPU power. | Verify the video engine is actually exposed and used. Don't equate “Intel i7” with universal codec support. [U2](#source-U2)[J3](#source-J3) |
| **SynoForum, February 16–18, 2026** | A NAS + Mac mini arrangement ran into certificate and port-routing problems after compute was separated. | Separation helps hardware choice but adds networking duties. Test TLS, proxy routes and real external playback. [U3](#source-U3) |
| **TrueNAS community, 2025 discussion** | Users asked about adding multiple disks and the behavior of RAIDZ expansion. | Treat current 25.10 documentation as authoritative; don't repeat older absolute claims that all RAIDZ growth requires a new vdev. [U4](#source-U4)[R8](#source-R8) |

Recurring practical issues across the sample and official guidance are **GPU visibility**, **network-share permissions**, **stable paths**, **remote-access certificates/routing**, and **misunderstanding expansion behavior**. This is not a quantified failure-rate claim. Sonarr/Radarr's own documentation also explicitly identifies path and permission pitfalls. [T1](#source-T1)[T2](#source-T2)

### The finished system's acceptance criteria

| Area | Pass condition | What a failure means |
|---|---|---|
| External account independence | Suspend/reset customer C without breaking A/B/D/E; old C credentials fail; active-session handling documented | Provider access model is not independently manageable. Do not sell the promise anyway. |
| Device compatibility | Exact target TVs/phones successfully play required video, audio, subtitles and HDR modes | Change client/profile or server capacity; a platform logo alone is not acceptance. |
| Five-viewer workload | Representative simultaneous direct-play/transcode sessions sustain playback and seeking within bandwidth/temperature limits | Limit workload or upgrade tested bottleneck; do not advertise untested counts. |
| Ten-gigabit storage path | Both NAS and host links negotiate 10Gb; a suitable transfer validates end-to-end throughput | Investigate card, switch, cable, storage and CPU—not just internet speed. |
| Safe storage expansion | Healthy pre-check; backup verified; supported drive added; job finishes; actual pool and volume capacities verified | Stop further additions and diagnose before risking another disk. |
| Second NAS | One catalog shows both sources; simulated loss of NAS2 leaves NAS1 content available without destructive catalog cleanup | Unification/failure handling needs correction; avoid spanned-pool assumptions. |
| Remote security / PIA | HTTPS/private access works from outside; required LAN traffic survives final VPN configuration; no public NAS admin page | Routing/security design is unfinished. |
| Recovery | A sample original and server configuration restore successfully to a safe location | Backup success notifications alone are insufficient. |

### What is verified, what is conditional, what is not done

**Verified from retrieved documentation:** product categories, principal platform listings, listed hardware, manufacturer-described expansion behaviors, the distinction between player activation and upstream authorization, and cited current pricing where explicitly labeled.

**Derived design decisions:** the ranking, suggested configuration, capacity arithmetic, headroom, bandwidth scenarios and cost totals. These are recommendations/calculations, not vendor promises.

**Still conditional:** exact NAS + 26 TB drive compatibility, current price/stock of models with allowance-only figures, every QNAP shelf/HBA maximum pairing, full populated noise/power comparison, your existing PC's hardware, your real provider permissions, and actual five-stream/codec testing. These gaps are flagged rather than concealed.

**Not performed:** purchases, NAS installation, provider provisioning, production security testing, or deployment to your personal computer. The delivered interactive HTML, PDFs and MP3 are the completed artifacts; they do not masquerade as a live streaming service.

### Final decisions

**External first:** choose independent upstream accounts/device tokens and prove individual revocation. Pilot a free compatible player; use iMPlayer for central device configuration where its supported platforms and license suit the deployment. Do not confuse its management tools with provider authority.

**Owned media when needed:** AS6810T + four approved equal CMR disks in RAID6 + separate Intel graphics-capable 10Gb media host. Jellyfin first; Plex only for a demonstrated client advantage with current terms/cost accepted. Grow within the chassis, then add a second independent NAS behind the same media library. One catalog, separate protected storage domains.

**Avoid the expensive mistake:** buying 200 TB of storage before confirming you want to own the files—and buying a replacement player before confirming where your current access problem actually lives.


## 12. Sources and purchasing references

All links were reviewed or surfaced during this research. Entries explicitly labeled limited retrieval or compatibility gate are not used as proof of unverified details. Community entries are opinions/experiences; retailer entries establish only their listed price/status. External links require internet; the report and explorer do not.

<section class="sources-grid">
<div class="source" id="source-F1"><strong>F1 · Flix Pro Player: activation, playlist management and reseller entry</strong><br>Official · Live page checked October 7, 2026<br><a href="https://flixproplayer.com/en-US">https://flixproplayer.com/en-US</a></div>

<div class="source" id="source-F2"><strong>F2 · iMPlayer: platforms, cloud management and pricing</strong><br>Official · Live page checked October 7, 2026<br><a href="https://implayer.tv/">https://implayer.tv/</a></div>

<div class="source" id="source-F3"><strong>F3 · Smarters Pro: supported platforms and feature tiers</strong><br>Official · Live page checked October 7, 2026<br><a href="https://smarterspro.com/">https://smarterspro.com/</a></div>

<div class="source" id="source-F4"><strong>F4 · TiviMate official player</strong><br>Official · Live page checked October 7, 2026<br><a href="https://tivimate.com/">https://tivimate.com/</a></div>

<div class="source" id="source-F5"><strong>F5 · Televizo official player</strong><br>Official · Live page checked October 7, 2026<br><a href="https://televizo.net/">https://televizo.net/</a></div>

<div class="source" id="source-F6"><strong>F6 · IPTVnator project: features and releases</strong><br>Official · Live page checked October 7, 2026<br><a href="https://github.com/4gray/iptvnator">https://github.com/4gray/iptvnator</a></div>

<div class="source" id="source-F7"><strong>F7 · Kodi: official downloads and platform list</strong><br>Official · Live page checked October 7, 2026<br><a href="https://kodi.tv/download/">https://kodi.tv/download/</a></div>

<div class="source" id="source-F8"><strong>F8 · VideoLAN: VLC official downloads</strong><br>Official; limited retrieval · Retrieval limited; confirm exact app-store version<br><a href="https://www.videolan.org/vlc/">https://www.videolan.org/vlc/</a></div>

<div class="source" id="source-F9"><strong>F9 · SS IPTV operator authentication integration</strong><br>Official · Live page checked October 7, 2026<br><a href="https://ss-iptv.com/en/operators/authorization">https://ss-iptv.com/en/operators/authorization</a></div>

<div class="source" id="source-F10"><strong>F10 · SS IPTV official service</strong><br>Official · Live page checked October 7, 2026<br><a href="https://ss-iptv.com/en/">https://ss-iptv.com/en/</a></div>

<div class="source" id="source-F11"><strong>F11 · SmartOne IPTV: platforms</strong><br>Official · Live page checked October 7, 2026<br><a href="https://smartone-iptv.com/">https://smartone-iptv.com/</a></div>

<div class="source" id="source-F12"><strong>F12 · SmartOne: device management</strong><br>Official · Live page checked October 7, 2026<br><a href="https://smartone-iptv.com/manage-devices">https://smartone-iptv.com/manage-devices</a></div>

<div class="source" id="source-F13"><strong>F13 · IBO Player: activation and device notes</strong><br>Official · Live page checked October 7, 2026<br><a href="https://frontend.iboplayer.com/news">https://frontend.iboplayer.com/news</a></div>

<div class="source" id="source-F14"><strong>F14 · IBO Player activation terms</strong><br>Official · Live page checked October 7, 2026<br><a href="https://activation.iboplayer.com/">https://activation.iboplayer.com/</a></div>

<div class="source" id="source-P1"><strong>P1 · Plex plans and remote-viewing eligibility</strong><br>Official · Checked October 7, 2026; Remote Watch pricing effective June 1, 2026<br><a href="https://www.plex.tv/plans/">https://www.plex.tv/plans/</a></div>

<div class="source" id="source-P2"><strong>P2 · Plex supported smart TVs</strong><br>Official · Updated January 21, 2025; checked October 7, 2026<br><a href="https://support.plex.tv/articles/204080173-which-smart-tv-models-are-supported/">https://support.plex.tv/articles/204080173-which-smart-tv-models-are-supported/</a></div>

<div class="source" id="source-P3"><strong>P3 · Plex app/platform list</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.plex.tv/apps-devices/">https://www.plex.tv/apps-devices/</a></div>

<div class="source" id="source-P4"><strong>P4 · Plex terms attached to software downloads</strong><br>Official · Terms dated October 30, 2025; checked October 7, 2026<br><a href="https://www.plex.tv/media-server-downloads/">https://www.plex.tv/media-server-downloads/</a></div>

<div class="source" id="source-J1"><strong>J1 · Jellyfin client directory</strong><br>Official · Live page checked October 7, 2026<br><a href="https://jellyfin.org/clients/">https://jellyfin.org/clients/</a></div>

<div class="source" id="source-J2"><strong>J2 · Jellyfin: all client downloads</strong><br>Official · Live page checked October 7, 2026<br><a href="https://jellyfin.org/downloads/clients/all/">https://jellyfin.org/downloads/clients/all/</a></div>

<div class="source" id="source-J3"><strong>J3 · Jellyfin hardware selection</strong><br>Official · Live page checked October 7, 2026<br><a href="https://jellyfin.org/docs/general/administration/hardware-selection/">https://jellyfin.org/docs/general/administration/hardware-selection/</a></div>

<div class="source" id="source-J4"><strong>J4 · Jellyfin client documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://jellyfin.org/docs/general/clients/">https://jellyfin.org/docs/general/clients/</a></div>

<div class="source" id="source-E1"><strong>E1 · Emby server and app downloads</strong><br>Official · Live page checked October 7, 2026<br><a href="https://emby.media/download.html">https://emby.media/download.html</a></div>

<div class="source" id="source-E2"><strong>E2 · Emby Premiere: pricing and device entitlement</strong><br>Official · Live page checked October 7, 2026<br><a href="https://emby.media/premiere.html">https://emby.media/premiere.html</a></div>

<div class="source" id="source-N1"><strong>N1 · ASUSTOR AS6810T hardware specifications</strong><br>Official · Indexed official specifications checked October 7, 2026; direct retrieval intermittently blocked<br><a href="https://www.asustor.com/product/spec?p_id=89">https://www.asustor.com/product/spec?p_id=89</a></div>

<div class="source" id="source-N2"><strong>N2 · ASUSTOR Lockerstor Gen3 product family</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.asustor.com/product/AS68">https://www.asustor.com/product/AS68</a></div>

<div class="source" id="source-N3"><strong>N3 · ASUSTOR AS6510T hardware specifications</strong><br>Official · Indexed official specifications; older model, current supply uncertain<br><a href="https://www.asustor.com/product/spec?p_id=64">https://www.asustor.com/product/spec?p_id=64</a></div>

<div class="source" id="source-N4"><strong>N4 · QNAP TS-1655 hardware specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qnap.com/en-us/product/ts-1655/specs/hardware">https://www.qnap.com/en-us/product/ts-1655/specs/hardware</a></div>

<div class="source" id="source-N5"><strong>N5 · Synology DS2422+ specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.synology.com/en-us/products/DS2422%2B">https://www.synology.com/en-us/products/DS2422%2B</a></div>

<div class="source" id="source-N6"><strong>N6 · Synology DS3622xs+ specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.synology.com/en-us/products/DS3622xs%2B">https://www.synology.com/en-us/products/DS3622xs%2B</a></div>

<div class="source" id="source-N7"><strong>N7 · QNAP TVS-AIh1688ATX product specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qnap.com/en-us/product/tvs-aih1688atx">https://www.qnap.com/en-us/product/tvs-aih1688atx</a></div>

<div class="source" id="source-N8"><strong>N8 · QNAP TVS-h874 hardware specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qnap.com/en-us/product/tvs-h874/specs/hardware">https://www.qnap.com/en-us/product/tvs-h874/specs/hardware</a></div>

<div class="source" id="source-N9"><strong>N9 · QNAP TS-1273AU-RP hardware specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qnap.com/en-us/product/ts-1273au-rp/specs/hardware">https://www.qnap.com/en-us/product/ts-1273au-rp/specs/hardware</a></div>

<div class="source" id="source-N10"><strong>N10 · QNAP TS-1232PXU-RP hardware specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qnap.com/en-us/product/ts-1232pxu-rp/specs/hardware">https://www.qnap.com/en-us/product/ts-1232pxu-rp/specs/hardware</a></div>

<div class="source" id="source-N11"><strong>N11 · Synology DS1825+ specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.synology.com/en-us/products/DS1825%2B">https://www.synology.com/en-us/products/DS1825%2B</a></div>

<div class="source" id="source-N12"><strong>N12 · ASUSTOR hardware compatibility selector</strong><br>Official; compatibility gate · Exact AS6810T + 26 TB SKU combination not independently confirmed<br><a href="https://www.asustor.com/services/hd">https://www.asustor.com/services/hd</a></div>

<div class="source" id="source-R1"><strong>R1 · ASUSTOR ADM volume management help</strong><br>Official · Official Japanese-language help checked October 7, 2026<br><a href="https://www.asustor.com/online/online_help?id=29&amp;lan=jpn">https://www.asustor.com/online/online_help?id=29&amp;lan=jpn</a></div>

<div class="source" id="source-R2"><strong>R2 · Synology storage expansion guide</strong><br>Official · Updated March 31, 2026<br><a href="https://kb.synology.com/DSM/tutorial/how_to_expand_storage">https://kb.synology.com/DSM/tutorial/how_to_expand_storage</a></div>

<div class="source" id="source-R3"><strong>R3 · QuTS hero 5.3: expand a RAID group with disks</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/expanding-a-storage-pool-by-adding-disks-to-a-raid-group-1D229DFC.html">https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/expanding-a-storage-pool-by-adding-disks-to-a-raid-group-1D229DFC.html</a></div>

<div class="source" id="source-R4"><strong>R4 · QNAP: individual disk expansion introduced in QuTS hero 5.1</strong><br>Official · Published September 19, 2023; checked October 7, 2026<br><a href="https://www.qnap.com/en-us/how-to/faq/article/can-i-add-an-individual-disk-to-expand-my-storage-pool-in-quts-hero-like-qts">https://www.qnap.com/en-us/how-to/faq/article/can-i-add-an-individual-disk-to-expand-my-storage-pool-in-quts-hero-like-qts</a></div>

<div class="source" id="source-R5"><strong>R5 · QuTS hero 5.3: add a new RAID group</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/expanding-a-storage-pool-by-adding-a-new-raid-group-A536B37F.html">https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/expanding-a-storage-pool-by-adding-a-new-raid-group-A536B37F.html</a></div>

<div class="source" id="source-R6"><strong>R6 · Unraid: adding disks to an array</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.unraid.net/unraid-os/using-unraid-to/manage-storage/array/adding-disks-to-array/">https://docs.unraid.net/unraid-os/using-unraid-to/manage-storage/array/adding-disks-to-array/</a></div>

<div class="source" id="source-R7"><strong>R7 · Unraid: array overview</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.unraid.net/unraid-os/using-unraid-to/manage-storage/array/overview/">https://docs.unraid.net/unraid-os/using-unraid-to/manage-storage/array/overview/</a></div>

<div class="source" id="source-R8"><strong>R8 · TrueNAS 25.10: pool management and RAIDZ expansion</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.truenas.com/docs/scale/25.10/scaletutorials/storage/managepoolsscale/">https://www.truenas.com/docs/scale/25.10/scaletutorials/storage/managepoolsscale/</a></div>

<div class="source" id="source-R9"><strong>R9 · mergerfs project documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://trapexit.github.io/mergerfs/">https://trapexit.github.io/mergerfs/</a></div>

<div class="source" id="source-R10"><strong>R10 · ASUSTOR AS6004U hardware specifications</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.asustor.com/th/product/AS6004U_belonging?tab=3">https://www.asustor.com/th/product/AS6004U_belonging?tab=3</a></div>

<div class="source" id="source-R11"><strong>R11 · AS6004U independent storage-space product notes</strong><br>Retailer · Retailer reproduction of manufacturer expansion notes; checked October 7, 2026<br><a href="https://www.adorama.com/ast6004u.html">https://www.adorama.com/ast6004u.html</a></div>

<div class="source" id="source-R12"><strong>R12 · QuTS hero 5.3: system storage pool</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/creating-a-storage-pool-F69691A3.html">https://docs.qnap.com/operating-system/quts-hero/5.3.x/en-us/creating-a-storage-pool-F69691A3.html</a></div>

<div class="source" id="source-C1"><strong>C1 · AS6810T US price and stock listing</strong><br>Retailer · Listing retrieved October 7, 2026; stock/price can change<br><a href="https://www.bhphotovideo.com/c/product/1869080-REG/asustor_as6810t_lockerstor_gen3_10_bay_nas.html">https://www.bhphotovideo.com/c/product/1869080-REG/asustor_as6810t_lockerstor_gen3_10_bay_nas.html</a></div>

<div class="source" id="source-C2"><strong>C2 · QNAP TS-1655 US listing</strong><br>Retailer · Listing retrieved October 7, 2026<br><a href="https://www.bhphotovideo.com/c/product/1745877-REG/qnap_ts_1655_8g_us_16bay_desktop_nas_intel_atom.html">https://www.bhphotovideo.com/c/product/1745877-REG/qnap_ts_1655_8g_us_16bay_desktop_nas_intel_atom.html</a></div>

<div class="source" id="source-C3"><strong>C3 · DS2422+ US listing</strong><br>Retailer · Listing retrieved October 7, 2026<br><a href="https://www.bhphotovideo.com/c/product/1674616-REG/synology_discstation_ds2422_12bay_nas.html/specs">https://www.bhphotovideo.com/c/product/1674616-REG/synology_discstation_ds2422_12bay_nas.html/specs</a></div>

<div class="source" id="source-C4"><strong>C4 · TVS-AIh1688ATX US listing</strong><br>Retailer · Listing retrieved October 7, 2026<br><a href="https://www.bhphotovideo.com/c/product/1928302-REG/qnap_tvs_aih1688atx_u9_48g_us_16_bay_quts_hero_nas.html/overview">https://www.bhphotovideo.com/c/product/1928302-REG/qnap_tvs_aih1688atx_u9_48g_us_16_bay_quts_hero_nas.html/overview</a></div>

<div class="source" id="source-C5"><strong>C5 · TS-1273AU-RP manufacturer store</strong><br>Manufacturer store · Listed $2,599; page also indicates preorder/lead time<br><a href="https://store.qnap.com/ts-1273au-rp-8g-us.html">https://store.qnap.com/ts-1273au-rp-8g-us.html</a></div>

<div class="source" id="source-C6"><strong>C6 · TS-1232PXU-RP US listing</strong><br>Retailer · Listing retrieved October 7, 2026<br><a href="https://www.bhphotovideo.com/c/product/1596836-REG/qnap_ts_1232pxu_rp_4g_us_qnap_2u_12_bay_arm_based.html/overview">https://www.bhphotovideo.com/c/product/1596836-REG/qnap_ts_1232pxu_rp_4g_us_qnap_2u_12_bay_arm_based.html/overview</a></div>

<div class="source" id="source-C7"><strong>C7 · AS6510T older-model marketplace listing</strong><br>Marketplace; conditional · Indexed new-stock offer $1,595; live inventory/warranty not confirmed<br><a href="https://www.ebay.com/itm/297619620269">https://www.ebay.com/itm/297619620269</a></div>

<div class="source" id="source-C8"><strong>C8 · WD Red Pro 26 TB price</strong><br>Retailer · Listed $1,144.99; checked October 7, 2026<br><a href="https://www.adorama.com/wd-red-pro-3-5-sata-iii-internal-nas-hard-drive-hdd-7200rpm/p/wd260kfgx">https://www.adorama.com/wd-red-pro-3-5-sata-iii-internal-nas-hard-drive-hdd-7200rpm/p/wd260kfgx</a></div>

<div class="source" id="source-C9"><strong>C9 · WD Red Pro 26 TB second price and availability</strong><br>Retailer · Listed $1,240.99; temporarily out of stock; checked October 7, 2026<br><a href="https://www.bhphotovideo.com/c/product/1875011-REG/wd_wd260kfgx_spcngn0_wd_red_pro_26tb.html/specs">https://www.bhphotovideo.com/c/product/1875011-REG/wd_wd260kfgx_spcngn0_wd_red_pro_26tb.html/specs</a></div>

<div class="source" id="source-C10"><strong>C10 · WD Red Pro 26 TB third price</strong><br>Retailer · Listed $1,312.99; checked October 7, 2026<br><a href="https://www.cdw.com/product/western-digital-red-pro-26tb-nas-hard-drive-3.5-sata-7200rpm-cmr/8268022">https://www.cdw.com/product/western-digital-red-pro-26tb-nas-hard-drive-3.5-sata-7200rpm-cmr/8268022</a></div>

<div class="source" id="source-A1"><strong>A1 · HandBrake: capabilities and copy-protection limitations</strong><br>Official · Live page checked October 7, 2026<br><a href="https://handbrake.fr/docs/en/1.9.0/introduction/about.html">https://handbrake.fr/docs/en/1.9.0/introduction/about.html</a></div>

<div class="source" id="source-A2"><strong>A2 · HandBrake: source formats including camera and analog captures</strong><br>Official · Live page checked October 7, 2026<br><a href="https://handbrake.fr/docs/en/1.8.0/technical/source-formats.html">https://handbrake.fr/docs/en/1.8.0/technical/source-formats.html</a></div>

<div class="source" id="source-A3"><strong>A3 · Silicondust HDHomeRun current lineup and DVR pricing</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.silicondust.com/hdhomerun.html">https://www.silicondust.com/hdhomerun.html</a></div>

<div class="source" id="source-A4"><strong>A4 · HDHomeRun FLEX 4K: DRM restrictions and price</strong><br>Official · Live page checked October 7, 2026<br><a href="https://shop.silicondust.com/shop/product/hdfx-4k/">https://shop.silicondust.com/shop/product/hdfx-4k/</a></div>

<div class="source" id="source-A5"><strong>A5 · Internet Archive help and download categories</strong><br>Official · Live page checked October 7, 2026<br><a href="https://help.archive.org/">https://help.archive.org/</a></div>

<div class="source" id="source-A6"><strong>A6 · Library of Congress Free to Use and Reuse: public-domain film selection</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.loc.gov/free-to-use">https://www.loc.gov/free-to-use</a></div>

<div class="source" id="source-A7"><strong>A7 · NASA media usage guidelines</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.nasa.gov/nasa-brand-center/images-and-media/">https://www.nasa.gov/nasa-brand-center/images-and-media/</a></div>

<div class="source" id="source-A8"><strong>A8 · Bandcamp purchase download formats</strong><br>Official · Published June 12, 2026<br><a href="https://get.bandcamp.help/en/articles/15263234-in-which-formats-can-i-download-my-purchases">https://get.bandcamp.help/en/articles/15263234-in-which-formats-can-i-download-my-purchases</a></div>

<div class="source" id="source-A9"><strong>A9 · Qobuz download store</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qobuz.com/us-en/shop">https://www.qobuz.com/us-en/shop</a></div>

<div class="source" id="source-A10"><strong>A10 · Netflix offline-download expiration rules</strong><br>Official · Live page checked October 7, 2026<br><a href="https://help.netflix.com/en/node/54865">https://help.netflix.com/en/node/54865</a></div>

<div class="source" id="source-A11"><strong>A11 · Tubi supported devices</strong><br>Official · Live page checked October 7, 2026<br><a href="https://tubitv.com/static/devices">https://tubitv.com/static/devices</a></div>

<div class="source" id="source-A12"><strong>A12 · Tubi: free supported-platform overview</strong><br>Official · Live page checked October 7, 2026<br><a href="https://tubitv.com/en-gb/welcome">https://tubitv.com/en-gb/welcome</a></div>

<div class="source" id="source-A13"><strong>A13 · Vimeo On Demand shutdown notice</strong><br>Official · New purchases stopped September 21, 2026; shutdown November 20, 2026<br><a href="https://vimeo.com/ondemand/shutdown">https://vimeo.com/ondemand/shutdown</a></div>

<div class="source" id="source-A14"><strong>A14 · Vimeo: downloadable existing purchases</strong><br>Official · Live page checked October 7, 2026<br><a href="https://help.vimeo.com/hc/en-us/articles/22089479757841-How-to-download-On-Demand-videos">https://help.vimeo.com/hc/en-us/articles/22089479757841-How-to-download-On-Demand-videos</a></div>

<div class="source" id="source-A15"><strong>A15 · U.S. Copyright Office: 2024 Section 1201 proceeding</strong><br>Official · 2024 rulemaking; checked October 7, 2026<br><a href="https://www.copyright.gov/1201/2024/">https://www.copyright.gov/1201/2024/</a></div>

<div class="source" id="source-A16"><strong>A16 · U.S. Copyright Office: anti-circumvention explanation</strong><br>Official · Historical statutory explanation; not a substitute for current exemptions<br><a href="https://www.copyright.gov/1201/2018/faqs.html">https://www.copyright.gov/1201/2018/faqs.html</a></div>

<div class="source" id="source-T1"><strong>T1 · Sonarr official documentation and path/permissions cautions</strong><br>Official · Live page checked October 7, 2026<br><a href="https://sonarr.tv/">https://sonarr.tv/</a></div>

<div class="source" id="source-T2"><strong>T2 · Radarr official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://radarr.video/">https://radarr.video/</a></div>

<div class="source" id="source-T3"><strong>T3 · Bazarr official project</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.bazarr.media/">https://www.bazarr.media/</a></div>

<div class="source" id="source-T4"><strong>T4 · Seerr official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.seerr.dev/">https://docs.seerr.dev/</a></div>

<div class="source" id="source-T5"><strong>T5 · Prowlarr official project</strong><br>Official · Live page checked October 7, 2026<br><a href="https://github.com/Prowlarr/Prowlarr">https://github.com/Prowlarr/Prowlarr</a></div>

<div class="source" id="source-T6"><strong>T6 · tinyMediaManager documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.tinymediamanager.org/docs/">https://www.tinymediamanager.org/docs/</a></div>

<div class="source" id="source-T7"><strong>T7 · Tautulli official project</strong><br>Official · Live page checked October 7, 2026<br><a href="https://tautulli.com/">https://tautulli.com/</a></div>

<div class="source" id="source-T8"><strong>T8 · Kometa official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://kometa.wiki/">https://kometa.wiki/</a></div>

<div class="source" id="source-T9"><strong>T9 · Tdarr official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://docs.tdarr.io/">https://docs.tdarr.io/</a></div>

<div class="source" id="source-T10"><strong>T10 · rclone official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://rclone.org/docs/">https://rclone.org/docs/</a></div>

<div class="source" id="source-T11"><strong>T11 · restic official documentation</strong><br>Official · Live page checked October 7, 2026<br><a href="https://restic.readthedocs.io/">https://restic.readthedocs.io/</a></div>

<div class="source" id="source-T12"><strong>T12 · Audiobookshelf official project</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.audiobookshelf.org/">https://www.audiobookshelf.org/</a></div>

<div class="source" id="source-V1"><strong>V1 · PIA Windows 10/11 setup, LAN and port-forwarding behavior</strong><br>Official · Published/updated September 2026; checked October 7, 2026<br><a href="https://helpdesk.privateinternetaccess.com/hc/en-us/articles/46565662533915-Windows-10-and-11-Installing-and-Using-the-PIA-App">https://helpdesk.privateinternetaccess.com/hc/en-us/articles/46565662533915-Windows-10-and-11-Installing-and-Using-the-PIA-App</a></div>

<div class="source" id="source-V2"><strong>V2 · PIA Android setup</strong><br>Official · Published/updated September 2026; checked October 7, 2026<br><a href="https://helpdesk.privateinternetaccess.com/hc/en-us/articles/46816642236443-Android-Installing-and-Setting-Up-the-PIA-App">https://helpdesk.privateinternetaccess.com/hc/en-us/articles/46816642236443-Android-Installing-and-Setting-Up-the-PIA-App</a></div>

<div class="source" id="source-U1"><strong>U1 · Reddit: NAS shares mounted by a separate Jellyfin host</strong><br>Community anecdote, not a benchmark · May 19, 2025<br><a href="https://www.reddit.com/r/homelab/comments/1kq0e1v/beginner_post/">https://www.reddit.com/r/homelab/comments/1kq0e1v/beginner_post/</a></div>

<div class="source" id="source-U2"><strong>U2 · Reddit: reused older PC and Quick Sync configuration problems</strong><br>Community anecdote, not a benchmark · April 3, 2026<br><a href="https://www.reddit.com/r/selfhosted/comments/1sb6b7j/where_to_start/">https://www.reddit.com/r/selfhosted/comments/1sb6b7j/where_to_start/</a></div>

<div class="source" id="source-U3"><strong>U3 · SynoForum: NAS plus Mac mini; reverse-proxy/certificate trouble</strong><br>Community anecdote · February 16–18, 2026<br><a href="https://www.synoforum.com/threads/nas-but-also-mac-mini.15775/">https://www.synoforum.com/threads/nas-but-also-mac-mini.15775/</a></div>

<div class="source" id="source-U4"><strong>U4 · TrueNAS forum: RAIDZ expansion discussion</strong><br>Community discussion · 2025 discussion; current behavior checked against TrueNAS 25.10 docs<br><a href="https://forums.truenas.com/t/raidz-expansion-multiple-disks-at-once/42675">https://forums.truenas.com/t/raidz-expansion-multiple-disks-at-once/42675</a></div>

<div class="source" id="source-D1"><strong>D1 · Internet Archive: using Archive BitTorrents</strong><br>Official · Live page checked October 7, 2026<br><a href="https://help.archive.org/help/archive-bittorrents/">https://help.archive.org/help/archive-bittorrents/</a></div>

<div class="source" id="source-D2"><strong>D2 · qBittorrent official project and downloads</strong><br>Official · Live page checked October 7, 2026<br><a href="https://www.qbittorrent.org/">https://www.qbittorrent.org/</a></div>

<div class="source" id="source-D3"><strong>D3 · qBittorrent official options: network-interface binding</strong><br>Official · Wiki edited September 3, 2026; checked October 7, 2026<br><a href="https://github.com/qbittorrent/qBittorrent/wiki/Explanation-of-Options-in-qBittorrent">https://github.com/qbittorrent/qBittorrent/wiki/Explanation-of-Options-in-qBittorrent</a></div>

<div class="source" id="source-D4"><strong>D4 · Prowlarr maintained definition: 1337x</strong><br>Official · Definition retrieved October 7, 2026; integration evidence, not an uptime or licensing test<br><a href="https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/1337x.yml">https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/1337x.yml</a></div>

<div class="source" id="source-D5"><strong>D5 · Prowlarr maintained definition: Nyaa.si</strong><br>Official · Definition retrieved October 7, 2026; integration evidence, not an uptime or licensing test<br><a href="https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/nyaasi.yml">https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/nyaasi.yml</a></div>

<div class="source" id="source-D6"><strong>D6 · Prowlarr maintained definition: TorrentLeech</strong><br>Official · Definition retrieved October 7, 2026; login and live account not tested<br><a href="https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/torrentleech.yml">https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/torrentleech.yml</a></div>

<div class="source" id="source-D7"><strong>D7 · Prowlarr maintained definition: EZTV</strong><br>Official · Definition retrieved October 7, 2026; primary hostname is eztvx.to<br><a href="https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/eztv.yml">https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/eztv.yml</a></div>

<div class="source" id="source-D8"><strong>D8 · Prowlarr maintained definition: YTS</strong><br>Official · Definition retrieved October 7, 2026; primary hostname is yts.gg<br><a href="https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/yts.yml">https://raw.githubusercontent.com/Prowlarr/Indexers/master/definitions/v11/yts.yml</a></div>

<div class="source" id="source-D9"><strong>D9 · SABnzbd official Usenet downloader</strong><br>Official · Live page checked October 7, 2026<br><a href="https://sabnzbd.org/">https://sabnzbd.org/</a></div>

<div class="source" id="source-D10"><strong>D10 · TorrentGalaxy staff describe prolonged outage and stopped bots</strong><br>Reported staff interview / TorrentFreak · March 14, 2025; historical outage report, not proof of October 2026 status<br><a href="https://torrentfreak.com/torrentgalaxy-staff-fear-the-worst-as-site-stays-dark-and-upload-bots-fail-250314/">https://torrentfreak.com/torrentgalaxy-staff-fear-the-worst-as-site-stays-dark-and-upload-bots-fail-250314/</a></div>

<div class="source" id="source-U5"><strong>U5 · Reddit: indexer recommendations, torrents versus Usenet</strong><br>Community discussion; qualitative sample · Reviewed October 7, 2026; retrieved page displays 9mo ago; exact publication date unavailable<br><a href="https://www.reddit.com/r/selfhosted/comments/1pq08vr/aaaarrrrr_where_be_ye_finding_indexers/">https://www.reddit.com/r/selfhosted/comments/1pq08vr/aaaarrrrr_where_be_ye_finding_indexers/</a></div>

<div class="source" id="source-U6"><strong>U6 · Reddit: Sonarr indexers and confusion between providers and indexers</strong><br>Community discussion; qualitative sample · Reviewed October 7, 2026; retrieved page displays 3mo ago; exact publication date unavailable<br><a href="https://www.reddit.com/r/sonarr/comments/1uq08pk/indexers/">https://www.reddit.com/r/sonarr/comments/1uq08pk/indexers/</a></div>

<div class="source" id="source-U7"><strong>U7 · Reddit: client-crash discussion and qBittorrent recommendations</strong><br>Community discussion; qualitative sample · Reviewed October 7, 2026; cached page displays 22h ago; not treated as a publication date<br><a href="https://www.reddit.com/r/torrents/comments/1wkn248/my_utorrent_keeps_crashing_randomly_while_a/">https://www.reddit.com/r/torrents/comments/1wkn248/my_utorrent_keeps_crashing_randomly_while_a/</a></div>

<div class="source" id="source-U8"><strong>U8 · Reddit: Radarr cleanup, hard links and continued seeding</strong><br>Community problem report; qualitative sample · Reviewed October 7, 2026; retrieved page displays 19d ago; exact publication date unavailable<br><a href="https://www.reddit.com/r/radarr/comments/1w9vmga/radarr_cleanup_solution/">https://www.reddit.com/r/radarr/comments/1w9vmga/radarr_cleanup_solution/</a></div>

<div class="source" id="source-U9"><strong>U9 · Reddit: wrong movie with same title and year</strong><br>Community problem report; unresolved, not a universal software defect · Reviewed October 7, 2026; retrieved page displays 16d ago; exact publication date unavailable<br><a href="https://www.reddit.com/r/radarr/comments/1w4u6tb/radarr_autograbbing_wrong_movie_same_movie_title/">https://www.reddit.com/r/radarr/comments/1w4u6tb/radarr_autograbbing_wrong_movie_same_movie_title/</a></div>

<div class="source" id="source-U10"><strong>U10 · Reddit: historical cartoon indexers and RARBG closure</strong><br>Community discussion; not current availability evidence · June 3, 2023; deliberately historical, reviewed October 7, 2026<br><a href="https://www.reddit.com/r/prowlarr/comments/13yuae6/good_indexers_for_2000_cartoons/">https://www.reddit.com/r/prowlarr/comments/13yuae6/good_indexers_for_2000_cartoons/</a></div>

</section>

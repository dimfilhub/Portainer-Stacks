# Portainer Stacks

## What is it about?

This is a portainer stacks set that I use for some services on my Synology NAS at home. I had some stacks ready and needed to deploy also for some friends so I decided to have them here in public for anyone that would need a starting point.
This is mainly not my work. I found different guides and different approaches on every docker service I needed. I just collected and made few changes in compose files to match my needs. 

## Before you start

Please have in mind the following:

It is advisable to create a group/user only for docker purposes and then use this PUID/PGID id when needed. 

In the same direction, if you use your Synology NAS to populate your media collection (for Plex, Emby or Jellyfin) it is a good practice to create a separate shared folder and appropriate folder tree for the relative containers to work well together

Last, but not least, it would also be helpful to create a separate docker bridge network to use when necessary for your docker containers. 

You can find plenty of guides to do all the above but an axcellent one and easy to follow is [the one from DrFrankenstein's Tech Stuff.](https://drfrankenstein.co.uk/category/initial-setup-7-2/). I have also used the rest of his guides and are guaranteed to work. Really a great starting point for your docker 'journey'...

## The files

There are .yaml files for the following services:
- [Adguard Home](./adguard-home/)
    - [host](./adguard-home/adguard-host.yaml) and [macvlan](./adguard-home/adguard-macvlan.yaml) network modes
- [*arr Apps](./arr-apps/) 
    - [Radarr](./arr-apps/radarr.yaml)
    - [Sonarr](./arr-apps/sonarr.yaml)
    - [Prowlarr](./arr-apps/prowlarr.yaml)
- [Bitmagnet](./bitmagnet/)
- [Deluge](./deluge/)
- [Diun](./diun/)
- [Dozzle](./dozzle/)
- [Emby](./emby/)
- [FlareSolverr](./flaresolverr/)
- [GlueTun](./flaresolverr/)
- [Gotify](./gotify/)
- [Homarr](./homarr/)
- [Homepage](./homepage/)
- [Jackett](./jackett/)
- [Mealie](./mealie/)
- [Nginx Proxy Manager](./nginx-proxy-manager/)
- [NZBGet](./nzbget/)
- [NZBHydra2](./nzbhydra2/)
- [Pi-Hole](./pihole/)
    - Official ([host](./pihole/official/pihole-host.yaml) and [macvlan](./pihole/official/pihole-macvlan.yaml) network modes)
    - Chris Crowe's Pi-Hole with Unbound:
        - [bridge network mode](./pihole/crhriscrowe-bridge/)
        - [host network mode](./pihole/chriscrowe-host/)
        - [macvlan network mode](./pihole/chriscrowe-macvlan/)
- [Pingvin Share](./pingvin/)
- [Plex](./pingvin/)
- [ProjectSend](./projectsend/)
- [qBittorrent](./qbittorrent/)
- [SABnzbd](./sabnzbd/)
- [Scrutiny](./scrutiny/)
- [Speedtest Tracker](./speedtest/)
- [Tautulli](./tautulli/)
- [Vaultwarden](./vaultwarden/)
- [Watchtower](./watchtower/)
- [Wordpress](./wordpress/)
- [WUD](./wud/)

There are some more README files to check with more details if needed.

### Please note:
>Containers that need to communicate through VPN because of ISP or other restrictions are redirected to GlueTun as network mode in my use case. You can see that in Deluge, qBittorrent, Prowlarr, Jackett, NZBHydra2 and Flaresolverr. So, you have to first deploy GlueTun with settings for your VPN provider and then deploy each of the above. If VPN is not needed or required for your purposes, just change network mode to something else e.g. the bridge network you created.


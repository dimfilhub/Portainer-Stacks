## [BitMagnet](https://bitmagnet.io)

A great self-hosted BitTorrent indexer. Very nice project, but still in early stages so you may find some issues. Definetely you should try BitMagnet if you rely a lot on torrents.

The yaml file is straight from [DrFrankenstein's guide](https://drfrankenstein.co.uk/bitmagnet-in-container-manager-on-a-synology-nas/) with minor changes from me after checking official BitMagnet site [configuration guide](https://bitmagnet.io/setup/configuration.html).

    Have in mind that you need a lot of space for this indexer. After a few weeks of crawling the database will become quite a few GB! According to official site it could go roughly 50GB of disk space per 10 million torrents.
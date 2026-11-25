<p align="center"><img src="https://vulpurr.com/logo.svg?v=2" width="96" alt="Vulpurr"></p>

<h1 align="center">Vulpurr Pool</h1>

<p align="center">The classic mining pool software behind <code>pool.vulpurr.com</code>.<br>
<a href="https://vulpurr.com/pool/">Pool stats</a> · <a href="https://vulpurr.com">Website</a> · <a href="https://t.me/vulpurr">Telegram</a></p>

**English** · [Русский](#русский)

A fork of [monero-pool by jtgrassie](https://github.com/jtgrassie/monero-pool). The upstream history is kept and the Vulpurr changes sit on top; the original README is in [README.monero-pool.md](README.monero-pool.md).

## What is different

- Per-rig statistics: the XMRig password (`-p`) is the rig name, and the stats page shows hashrate per rig and per server.
- Hashrates decay to zero on their own when a miner or a downstream pool stops sending shares, instead of freezing at the last value.
- An updated built-in web UI.

Connect XMRig to the public pool:

```bash
xmrig -a rx/0 -o pool.vulpurr.com:3333 -u YOUR_VU_ADDRESS -p rig-name
```

Add `--tls` for encryption; use port 443 if your ISP blocks 3333. Fee 1%, payouts from 1 VUP every 10 minutes. Want zero fees? Mine with [P2Pool](https://github.com/vulpurr-network/vulpurr-p2pool) in the wallet.

## License

BSD 3-Clause, like the original ([LICENSE](LICENSE)). Thanks to jtgrassie.

---

## Русский

Код классического пула `pool.vulpurr.com`, форк [monero-pool от jtgrassie](https://github.com/jtgrassie/monero-pool). Что добавлено: статистика по каждому ригу (имя рига — пароль в XMRig), хешрейт сам уходит в ноль, когда майнер перестал присылать шары, и обновлённый веб-интерфейс. Комиссия 1%, выплаты от 1 VUP каждые 10 минут. Лицензия BSD 3-Clause.

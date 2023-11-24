# isucon11q-practice
本リポジトリは [isucon/isucon11-qualify: ISUCON11 予選 (ISUCONDITION)](https://github.com/isucon/isucon11-qualify) と [matsuu/ansible-isucon: Ansible playbooks for ISUCON](https://github.com/matsuu/ansible-isucon) を参考に作成したISUCON11予選の素振り環境コード置き場です。

## リンク集
- [ISUCON11 予選レギュレーション](https://isucon.net/archives/55854734.html)
- [ISUCON11 予選 当日マニュアル](https://github.com/isucon/isucon11-qualify/blob/main/docs/manual.md)

# コンパイルとサービス再起動
```bash
cd webapp/go/
go build -o isucondition && sudo systemctl restart isucondition.go.service
```

# ベンチマーク
```bash
cd bench
./bench -all-addresses 127.0.0.11 -target 127.0.0.11:443 -tls -jia-service-url http://127.0.0.1:4999
```

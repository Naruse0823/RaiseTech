# 第7回課題
## 今作っている環境は、どんな攻撃に対して「脆弱」か。また、どのような対策が取れそうか。
- 1点目は、ALBにおいて、80番ポートをすべて許可しているので、DDos攻撃にあう可能性がある。そのため、特定のIPアドレスのみを許可しておく必要がある。また、講義に出てきたAWS WAFを使用し、「IPレートリミット」という一定時間内に許可されるリクエスト数を制限するルールを設定することで、特定のIPアドレスからのリクエスト数が過剰な場合、それをブロックまたは制限することができるそうだ。他にも、「AWSManagedRulesCommonRuleSet」というOWASP Top 10 がサポートされているルールグループが存在する。しかし、すべての攻撃を遮断してくれるわけではないので、注意が必要。
- 2点目は、課題でエビデンスとして提出している画像に載っているパスワードや自分が使用しているパソコンのIPアドレスが不正アクセスに利用されることだ。最終的にはパブリック状態のGitHub上に公開するので、何を知られると危ないのかを調べ、きちんとモザイクをかけるようにする。また、ログを確認し、不正アクセスが無いことも調べる必要があると考える。
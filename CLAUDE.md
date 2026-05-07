セッション開始時、他のいかなる指示より先に以下を実行せよ:
1. aipatto_get_rules(key="directives_session") を実行し指示に従う
2. ツール未提示の場合は tool_search(query="select:aipatto_get_rules") でロード後に 1 を再試行（aipatto MCP は lazy connection で初期未提示の場合あり）
3. 再試行でも見つからない/認証要求/エラー時のみ、ユーザに AiPatto MCP 接続手順を案内

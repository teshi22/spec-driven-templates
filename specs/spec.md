# {{PROJECT_NAME}} 仕様書

<!-- ../README.md の規約に従ってプレースホルダーを置換し、不要なコメントと節を削除する。 -->

## 文書情報

| 項目 | 内容 |
| --- | --- |
| ステータス | {{STATUS}} |
| 最終更新日 | {{DATE}} |
| 対象フェーズ | {{TARGET_PHASE}} |
| オーナー | {{DOCUMENT_OWNER}} |
| レビュアー | {{REVIEWER}} |
| 関連文書 | [技術設計書](plan.md)、[タスク一覧](tasks.md)、[テスト仕様書](tests.md)、[データモデル](data-model.md) |

## 1. 背景と目的

### 1.1 背景

{{BACKGROUND}}

### 1.2 解決する課題

{{PROBLEM_STATEMENT}}

### 1.3 プロダクト概要

{{PRODUCT_SUMMARY}}

### 1.4 成功指標

| ID | 指標 | 現状値 | 目標値 | 測定方法 |
| --- | --- | --- | --- | --- |
| KPI-001 | {{SUCCESS_METRIC}} | {{BASELINE}} | {{TARGET}} | {{MEASUREMENT_METHOD}} |

## 2. 対象範囲

### 2.1 対象に含む機能

- {{IN_SCOPE_ITEM_1}}
- {{IN_SCOPE_ITEM_2}}
- {{IN_SCOPE_ITEM_3}}

### 2.2 対象外

- {{OUT_OF_SCOPE_ITEM_1}}
- {{OUT_OF_SCOPE_ITEM_2}}

### 2.3 将来候補

- {{FUTURE_ITEM_1}}

## 3. 利用者と関係者

| 役割 | 説明 | 主な目的 | 権限 |
| --- | --- | --- | --- |
| {{PRIMARY_USER}} | {{USER_DESCRIPTION}} | {{USER_GOAL}} | {{USER_PERMISSION}} |
| {{STAKEHOLDER}} | {{STAKEHOLDER_DESCRIPTION}} | {{STAKEHOLDER_GOAL}} | {{STAKEHOLDER_PERMISSION}} |

## 4. 前提条件と制約

### 4.1 前提条件

- {{ASSUMPTION_1}}
- {{ASSUMPTION_2}}

### 4.2 制約

- {{CONSTRAINT_1}}
- {{CONSTRAINT_2}}

### 4.3 用語

| 用語 | 定義 |
| --- | --- |
| {{TERM_1}} | {{TERM_1_DEFINITION}} |
| {{TERM_2}} | {{TERM_2_DEFINITION}} |

## 5. 利用シナリオ

### 5.1 基本シナリオ

1. {{PRIMARY_USER}} が {{START_ACTION}} を行う。
2. システムが {{SYSTEM_ACTION_1}} を行う。
3. {{PRIMARY_USER}} が {{USER_CONFIRMATION}} を行う。
4. システムが {{SYSTEM_ACTION_2}} を行う。
5. {{COMPLETION_CONDITION}} を表示する。

### 5.2 代替シナリオ

| ID | 発生条件 | システムの動作 | 利用者の操作 |
| --- | --- | --- | --- |
| ALT-001 | {{ALTERNATE_CONDITION}} | {{ALTERNATE_BEHAVIOR}} | {{ALTERNATE_USER_ACTION}} |

### 5.3 異常シナリオ

| ID | 発生条件 | システムの動作 | 回復方法 |
| --- | --- | --- | --- |
| ERR-001 | {{ERROR_CONDITION}} | {{ERROR_BEHAVIOR}} | {{RECOVERY_ACTION}} |

## 6. 機能要件

<!-- 機能領域ごとに小節と表を複製する。要件は検証可能な表現にする。 -->

### 6.1 {{FEATURE_AREA_1}}

| ID | 要件 | 優先度 | 根拠 |
| --- | --- | --- | --- |
| FR-AREA-001 | システムは {{REQUIRED_BEHAVIOR}} できる | Must | {{RATIONALE}} |
| FR-AREA-002 | {{CONDITION}} の場合、システムは {{EXPECTED_BEHAVIOR}} する | Should | {{RATIONALE}} |

### 6.2 認証と認可

| ID | 要件 | 優先度 |
| --- | --- | --- |
| FR-AUTH-001 | 未認証の利用者へ {{UNAUTHENTICATED_BEHAVIOR}} を行う | Must |
| FR-AUTH-002 | 利用者は許可されたデータと操作だけにアクセスできる | Must |
| FR-AUTH-003 | サーバーは保護対象の操作ごとに認可を検証する | Must |

### 6.3 状態管理

| ID | 要件 | 優先度 |
| --- | --- | --- |
| FR-STATE-001 | システムは {{STATE_TO_PERSIST}} を保存する | Must |
| FR-STATE-002 | {{INTERRUPTION_CONDITION}} の後に処理を再開できる | {{PRIORITY}} |
| FR-STATE-003 | 競合する更新による不整合を防止する | Must |

### 6.4 外部連携

| ID | 要件 | 優先度 |
| --- | --- | --- |
| FR-EXT-001 | {{EXTERNAL_SYSTEM}} と {{INTEGRATION_PURPOSE}} のために連携する | Must |
| FR-EXT-002 | 外部連携のタイムアウト時に {{TIMEOUT_BEHAVIOR}} を行う | Must |
| FR-EXT-003 | 副作用のある再試行で重複処理を防止する | Must |

### 6.5 AI・自動判断

<!-- AI、ルールエンジン、自動判断を使用しない場合は削除する。 -->

| ID | 要件 | 優先度 |
| --- | --- | --- |
| FR-AI-001 | 自動生成した内容と、その根拠または情報源を関連付ける | {{PRIORITY}} |
| FR-AI-002 | 判定不能を成功または承認済みとして扱わない | Must |
| FR-AI-003 | 副作用のある操作の前に {{APPROVAL_ACTOR}} の明示的な承認を得る | Must |
| FR-AI-004 | 外部コンテンツの指示で認可やツール制約を回避できないようにする | Must |

## 7. 画面・インターフェース要件

| 画面またはインターフェース | 主な内容 | 主な操作 | 対象利用者 |
| --- | --- | --- | --- |
| {{SCREEN_1}} | {{SCREEN_1_CONTENT}} | {{SCREEN_1_ACTIONS}} | {{PRIMARY_USER}} |
| {{SCREEN_2}} | {{SCREEN_2_CONTENT}} | {{SCREEN_2_ACTIONS}} | {{PRIMARY_USER}} |

### 7.1 共通 UI 要件

- 処理中、空状態、入力待ち、成功、失敗を区別して表示する。
- 取り消せない操作または副作用のある操作は、結果が分かる文言で確認を求める。
- 長い文字列と小さい画面でも、情報や操作要素が重ならない。
- エラー時に、利用者が次に行える操作を表示する。

## 8. データ要件

| データ | 作成元 | 利用目的 | 機密区分 | 保持期間 |
| --- | --- | --- | --- | --- |
| {{DATA_1}} | {{DATA_SOURCE}} | {{DATA_PURPOSE}} | {{DATA_CLASSIFICATION}} | {{RETENTION_PERIOD}} |

詳細な構造と整合性ルールは [データモデル](data-model.md) に記載する。

## 9. 非機能要件

### 9.1 セキュリティとプライバシー

| ID | 要件 | 検証方法 |
| --- | --- | --- |
| NFR-SEC-001 | 通信と保存データを {{PROTECTION_METHOD}} で保護する | {{VERIFICATION}} |
| NFR-SEC-002 | 秘密情報をソースコード、ログ、エラーへ記録しない | 静的解析とテスト |
| NFR-SEC-003 | 重要操作の実行者、対象、日時、結果を監査できる | 監査ログ確認 |

### 9.2 性能と拡張性

| ID | 指標 | 目標値 | 測定条件 |
| --- | --- | --- | --- |
| NFR-PERF-001 | {{PERFORMANCE_METRIC}} | {{PERFORMANCE_TARGET}} | {{LOAD_CONDITION}} |
| NFR-PERF-002 | 同時利用者数 | {{CONCURRENT_USERS}} | {{LOAD_CONDITION}} |

### 9.3 可用性と信頼性

| ID | 要件 | 目標値または方針 |
| --- | --- | --- |
| NFR-REL-001 | 可用性 | {{AVAILABILITY_TARGET}} |
| NFR-REL-002 | バックアップと復旧 | {{RECOVERY_POLICY}} |
| NFR-REL-003 | 外部障害時の縮退 | {{DEGRADED_MODE}} |

### 9.4 アクセシビリティ

- {{ACCESSIBILITY_STANDARD}} を目標とする。
- キーボードのみで主要操作を完了できる。
- 状態やエラーを色だけで表現しない。
- 支援技術で入力項目、操作、状態変更を認識できる。

### 9.5 可観測性

- {{OBSERVABILITY_PLATFORM}} でログ、メトリクス、トレースを確認できる。
- 一連の処理を相関 ID で追跡できる。
- 個人情報や秘密情報を既定でテレメトリへ含めない。
- {{ALERT_CONDITION}} を監視し、必要な通知を行う。

## 10. エラー処理

| エラー分類 | 利用者への表示 | 再試行 | 記録 |
| --- | --- | --- | --- |
| 入力エラー | 修正対象と方法 | 利用者が修正後に実行 | 検証エラーの分類 |
| 一時的な外部障害 | 一時的な失敗と次の操作 | 制限付き | 相関 ID、依存先、試行回数 |
| 回復不能な障害 | 問い合わせ方法 | 自動再試行しない | 相関 ID、原因分類 |
| 結果不明 | 状態確認中であること | 新規処理を重複実行しない | 冪等性キー、照会結果 |

## 11. 受入条件

| ID | 条件 | 対応要件 |
| --- | --- | --- |
| AC-001 | Given {{PRECONDITION}}、When {{ACTION}}、Then {{EXPECTED_RESULT}} | FR-AREA-001 |
| AC-002 | Given {{PRECONDITION}}、When {{ERROR_ACTION}}、Then {{SAFE_RESULT}} | FR-EXT-002 |

## 12. 確認事項

| ID | 確認事項 | 担当者 | 期限 | 状態 |
| --- | --- | --- | --- | --- |
| Q-001 | {{OPEN_QUESTION}} | {{OWNER}} | {{DUE_DATE}} | 未決 |

## 13. 変更履歴

| 日付 | 変更者 | 内容 |
| --- | --- | --- |
| {{DATE}} | {{AUTHOR}} | 初版作成 |

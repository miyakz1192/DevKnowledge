# Tech（技術領域の教訓）

IPA「情報処理システム高信頼化教訓集（ITサービス編）」の技術領域（T1〜T33）の教訓を、1ファイル1教訓で整理したもの。
ディレクトリはISO/IEC/IEEE 15288:2023（JIS X 0170）のライフサイクルプロセスに対応する（名称末尾の "Process" は省略）。
各教訓は、その教訓で示される予防策・対策が主に属するプロセスに1つだけ配置している。

| 教訓番号 | SLCPプロセス | ファイル | 教訓タイトル |
|---|---|---|---|
| T27 | Acquisition Process（6.1.1） | [BuyPackageSupport](Acquisition/BuyPackageSupport.md) | パッケージはサポートを買え |
| T9 | Risk Management Process（6.3.4） | [PrepareWorkarounds](RiskManagement/PrepareWorkarounds.md) | 検証は万全？それでもシステム障害は起こる。回避策を準備しておくこと |
| T5 | Configuration Management Process（6.3.5） | [ServiceChangeControl](ConfigurationManagement/ServiceChangeControl.md) | サービスの視点で、「変更管理」の仕組み作りと「品質管理責任」の明確化を！ |
| T29 | System Requirements Definition Process（6.4.3） | [AlignLimitDefinition](SystemRequirementsDefinition/AlignLimitDefinition.md) | 単位などの定義が異なる制限値、連携するシステム間で使っていませんか？ |
| T1 | System Architecture Definition Process（6.4.4） | [IsolateSuspectParts](SystemArchitectureDefinition/IsolateSuspectParts.md) | サービスの継続を優先するシステムにおいては、疑わしき構成要素を積極的にシステムから切り離せ（“フェールソフト”の考え方） |
| T2 | System Architecture Definition Process（6.4.4） | [BirdsEyeFailover](SystemArchitectureDefinition/BirdsEyeFailover.md) | 蟻の目だけでなく、システム全体を俯瞰する鳥の目で総合的な対策を行うべし！ |
| T10 | System Architecture Definition Process（6.4.4） | [LimitMeshScope](SystemArchitectureDefinition/LimitMeshScope.md) | メッシュ構成の範囲は、可用性の確保と、障害の波及リスクのバランスを勘案して決定する |
| T24 | System Architecture Definition Process（6.4.4） | [PlanForDegradation](SystemArchitectureDefinition/PlanForDegradation.md) | サービス縮退時の対策を考慮せよ |
| T19 | Design Definition Process（6.4.5） | [TameQueryOptimizer](DesignDefinition/TameQueryOptimizer.md) | リレーショナルデータベース（RDBMS）のクエリ自動最適化機能の適用は慎重に！ |
| T23 | Design Definition Process（6.4.5） | [MultiViewMonitoring](DesignDefinition/MultiViewMonitoring.md) | 障害監視は、複数の観点から実装し、障害の見逃しを防げ！ |
| T26 | Design Definition Process（6.4.5） | [ReuseWithPremises](DesignDefinition/ReuseWithPremises.md) | 既存システムの流用開発はその前提条件を十分把握し、そのまま利用可能な部分と変更する部分を調査して実施する |
| T33 | Design Definition Process（6.4.5） | [ExclusiveControl](DesignDefinition/ExclusiveControl.md) | 入念な方式設計と多段階の確認は当たり前、個人情報を扱う場合には特に排他制御に気をつけて |
| T20 | Implementation Process（6.4.7） | [CustomizeWithCare](Implementation/CustomizeWithCare.md) | パッケージ製品の機能カスタマイズはリスクを認識し特に必要十分なチェック体制やチェック手順を整備して進めること |
| T30 | Implementation Process（6.4.7） | [NoBundledRedundancy](Implementation/NoBundledRedundancy.md) | 意味がない、一緒に束ねた2重化配線！ |
| T18 | Integration Process（6.4.8） | [LegacyLinkSpecCheck](Integration/LegacyLinkSpecCheck.md) | 新たなサブシステムと老朽化した既存システムとを連携する場合は両者の仕様整合性を十分確認すべし |
| T3 | Verification Process（6.4.9） | [SimulateFieldMoves](Verification/SimulateFieldMoves.md) | 現場をよく知り、現場の知識を集約し、現場の動きをシミュレートできるようにすべし！ |
| T6 | Verification Process（6.4.9） | [TestProdEnvDiff](Verification/TestProdEnvDiff.md) | テスト環境と本番環境の差異を体系的に整理し、障害のリスク対策を練る |
| T14 | Transition Process（6.4.10） | [CheckWebPagePerf](Transition/CheckWebPagePerf.md) | Webページ更新時には、応答速度の変化等、性能面のチェックも忘れずに |
| T13 | Validation Process（6.4.11） | [ScenarioBasedTest](Validation/ScenarioBasedTest.md) | 利用者の観点に立った、業務シナリオに即したレビュー、テストが重要 |
| T7 | Operation Process（6.4.12） | [StandbyIsProduction](Operation/StandbyIsProduction.md) | バックアップ切替えが失敗する場合を考慮すべし |
| T8 | Operation Process（6.4.12） | [VirtualResourceMon](Operation/VirtualResourceMon.md) | 仮想サーバになってもリソース管理、性能監視は運用の要である |
| T11 | Operation Process（6.4.12） | [DetectSilentFailure](Operation/DetectSilentFailure.md) | サイレント障害を検知するには、適切なサービス監視が重要 |
| T15 | Operation Process（6.4.12） | [EmergencyDataSync](Operation/EmergencyDataSync.md) | 緊急時こそ、データの一貫性を確保するよう注意すべし |
| T22 | Operation Process（6.4.12） | [MonitorHiddenBuffers](Operation/MonitorHiddenBuffers.md) | 隠れたバッファの存在を把握し、目的別のしきい値設定と超過アラート監視でオーバフローを未然に防止すること |
| T31 | Operation Process（6.4.12） | [KeepRunbookCurrent](Operation/KeepRunbookCurrent.md) | 復旧手順は、システムとその環境の変化に対応させ常に最新に！ |
| T4 | Maintenance Process（6.4.13） | [ManageChangePoints](Maintenance/ManageChangePoints.md) | システムに影響する変化点を明確にし、その管理ルールを策定せよ！ |
| T12 | Maintenance Process（6.4.13） | [VerifyCompatParts](Maintenance/VerifyCompatParts.md) | 新製品は、旧製品と同一仕様と言われても、必ず差異を確認！ |
| T16 | Maintenance Process（6.4.13） | [FrequentPatchCheck](Maintenance/FrequentPatchCheck.md) | システム構成機器の修正パッチ情報の収集は頻繁に行い、緊急性に応じて計画的に対応すべし |
| T17 | Maintenance Process（6.4.13） | [PeriodicReboot](Maintenance/PeriodicReboot.md) | 長時間連続運転による不安定動作発生の回避には定期的な再起動も有効！ |
| T21 | Maintenance Process（6.4.13） | [InstructorChecksWork](Maintenance/InstructorChecksWork.md) | 作業ミスを減らすためには、作業指示者と作業者の連携で漏れのない対策を！ |
| T25 | Maintenance Process（6.4.13） | [PrepForUnknownCause](Maintenance/PrepForUnknownCause.md) | 障害原因が不明でも再発予防と発生時対策はできる |
| T28 | Maintenance Process（6.4.13） | [PackageUpdateCheck](Maintenance/PackageUpdateCheck.md) | パッケージを更新する時は、変更内容の詳細確認と回帰テストで二重に安全を確保せよ |
| T32 | Maintenance Process（6.4.13） | [WatchCycleTime](Maintenance/WatchCycleTime.md) | 周期処理、「時間」と「変化」を監視せよ！ |

出典：https://www.ipa.go.jp/archive/digital/iot-en-ci/system/lesson.html

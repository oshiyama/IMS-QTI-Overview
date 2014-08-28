IMS-QTI-Overview
================

IMS質問とテスト相互運用方法概要

バージョン: 2.1 最終版

発効日: 2012年8月31日

最終バージョン:  http://www.imsglobal.org/question/

知的所有権および配布での注意事項

この文書の受領者は、文書に規定された仕様の明らかな権利侵害を発見した場合、コメント、関連特許または知的所有権の通知、さらにそそれを裏付けるドキュメントを提出してください。

IMSは、当文書に記述されている技術の実装ないし利用に関して、主張されたいかなる知的所有権またはその他の権利について、あるいはその延長上のライセンス有無の正当性や範囲に関して、明確な立場は表明しません。また、それらの権利を明確化する努力もしません。IMSの仕様書にある権利行使に関する手順は、こちらをご覧ください。

http://www.imsglobal.org/ipr/imsipr_policyFinal.pdf

Copyright © 2005-2012 IMS Global Learning Consortium. All Rights Reserved.

この仕様書を使った製品またはサービスの開発は、次のIMSライセンスに従ってください。

http://www.imsglobal.org/license.html

必要に応じて提案書依頼 (RFP) を作成することで、いかなる団体へもこの文書の引用を許可します。
一旦与えられた制限付き許可は、恒久的でIMSを含むいかなる者もこれを撤回することはできません。
当仕様書には保障 (warranty) は付与されません。利用に際しては、すべて利用者のリスクで行ってください。コンソーシアム、会員、なららびに執筆者は、この仕様を用いた実装や第三者へのいかなる直接的・間接的損害に対しての責任は負いかねます。

QTI公開フォーラムへの発言やコメント投稿はこちらまで:

http://www.imsglobal.org/community/forum/categories.cfm?catid=52 


目次

1. 質問とテスト相互運用方法
1.1. 仕様書の歴史
1.2. 範囲
2. ユースケース
2.1. ユースケースアクター
3. 仕様構成
4. 適合性、拡張性、仕様とプロファイル管理
4.1 拡張方法
5. 最新変更点
6. 参照
　　

1. 質問とテスト相互運用方法

質問とテスト相互運用方法 (QTI)仕様書は、質問(評価項目)とテスト（評価テスト）のデータおよびその結果報告を説明するデータモデルを記述しています。
この仕様によって、項目、テストおよび結果をオーサリングツール、項目保管場所、テスト構築ツール、学習システムや評価配信システム間で交換可能になります。
データモデルは抽象的に記述され、UMLを使用して幅広いデータモデルツールとプログラミング言語を結合しますが、システム間の相互変換に、業界標準であるXML (eXtensible Markup Language)を結合に用いることができ、この結合方法を強く推奨します。 
IMS質問とテスト相互運用方法 (QTI)仕様書は、明確に定義された拡張ポイント規定を通して、相互運用性および革新の両方を支援します。これらの拡張ポイントは、特別なあるいは独自データを隠蔽するのに利用することができ、並びの項目を直接表現することができます。

1.1 仕様書の歴史

初期のV0.5仕様は、1999年3月に議論用として公開され、同年11月にIMS質問とテスト相互運用方法V1.0の開発で合意。続いて、2000年2月に公開ドラフト、同年5月に最終仕様として公開されました。
仕様書は、2001年3月と2002年1月の二回に渡りそれぞれで拡張・更新が行われ、同年2月には、6,000を超えるIMS QTI 1.x仕様が、IMSウェブサイトよりダウンロードされました。
それ以来、実装者からは多くの問題提起がなされ、それらはQTIプロジェクトチームによってレビューされました。それらの多くは適切に対処されたうえで、2003年3月に公開された仕様V1.2.1の付録に掲載されました。しかし、一部は、後方互換性を欠く仕様変更を必要とするか、問題解決のため引き続く解明ないし大幅な仕様拡張を必要とするようなより根源的問題提起であったために、同様には対処できませんでした。

QTI仕様が最初に着想されてからは、IMS仕様は幅広く成長し、コンテンツパッケージング、単一配列、そして最も新しくは学習設計の作業が加わるとともに、仕様書間を見直す必要が出てきました。2003年に見直しが行われた際、QTIに関する幾つかの整合性の問題を確認しました。同年9月、1.Xからの修正および整合性問題に対処してQTI V2.0を起草するプロジェクト憲章が合意されました。作業を管理可能にし且つ結果をできるだけ早期に確実にコミュニティに戻すため、、するべき作業範囲にいくつか制限事項を設定しました。そのため、QTI V2.0仕様公開時には、個々の評価項目 (AssessmentItem) に集中する一方、項目のセクションやテストへの集計や結果報告の部分は更新しませんでした。このQTI V2.1仕様公開では、QTI仕様の残りの部分を全て置き換えることによって1.xから2.xへの更新を完了しました。


1.2. 範囲

IMS QTIは、特にコンテンツプロバイダ(質問とテストの著者・出版社)、オーサリングツールやコンテンツ管理ツール、評価配信システムや学習システムの各開発者に関係します。質問主体コンテンツを表現するデータモデルは、すべての年齢層と各国のコンテキスト間での学習、教育および研修を目的とするユーザをターゲットとするのに適しています。

2. ユースケース

QTIは、ここに記述されている複数のシステムと、これらのシステムを利用するアクター間の相互運用性を促進するように設計されています。
特に、QTIは次の目的で設計されています。

●　オーサリングツールと独立させた、項目の蓄積と交換のためのコンテンツフォーマットの十分な文書化

●　幅広い学習評価システムを網羅する項目保管場所 (item banks)の展開支援

●　テスト構築ツールと独立させた、テストの蓄積と交換のためのコンテンツフォーマットの十分な文書化

●　単一の学習システムまたは評価配信システムにおける多様なソースからの項目、項目保管場所(item banks)やテストの展開支援

●　一貫性を持ってテスト結果を報告する能力を備えたシステムの提供



components

Figure 2.1 テスト評価と項目評価の役割 (The Role of Assessment Tests and Assessment Items)


オーサリングツール (authoringTool)
著者が、評価項目の作成・更新のために利用するシステム

項目保管場所 (itemBank)
評価項目の集合を、収集ないし管理するためのシステム

テスト構築ツール (testConstructionTool)
個別の項目からテストを組み立てるためのシステム

評価配信システム (assessmentDeliverySystem)
候補者への評価配信管理システム。システムには候補者へ項目を配信したり、返答を必要に応じて自動的に集計するなり結果を集計者へ届けたりする配信エンジンが含まれます。

学習システム (learningSystem)
教師と一緒になって、生徒を学習活動に導くシステム。当仕様書の目的として、生徒は学習システムとのやり取りの中で（例えば形成的評価）項目評価を知る機会を得ますが、これが形成的かまたは累積的評価が為されたかといえば、正式には区別がされてなくて候補に留まります。学習システムには、管理用の配信エンジンが含まれていると見なされますが、評価配信システムとはセキュリティモデルが大きく異なります。

2.1 ユースケースアクター
当仕様書で規定されている役割に関しては、少数の抽象アクターに簡素化しました。実際の学習や評価システムにおいては役割はずっと複雑になりますが、仕様書の目的として、ここで規定される役割の一つ一つが実際の場面では一般化されると想定しています。

著者 (author)
項目評価の作成者。単純な状況下では、一項目に著者は一人。もっと複雑な状況下では、一項目にたいして、作成および品質管理プロセスを通して多くの人が係る。当仕様書では、ここに係る人すべてを著者と扱います。著者は評価内容に係りますが、項目保管管理者(itemBankManager)とは区別します。著者はオーサリングツールを通して項目に接します。

項目保管管理者(itemBankManager)
項目保管場所にある評価項目の集合に管理責任を持つアクター

テスト構築者(testConstructor)
テスト構築者の役割は、個々の項目からテスト（またはテストフォーム)を作成することです。項目は、通常は項目保管場所から引き出してきます。


試験監督官(proctor)
評価配信を監視する人。多くの場合、試験監督と呼ばれる。当仕様書の目的のために、試験監督官は、この配信プロセスに係る者であれば候補以外の誰でもがなれます。一方、候補者からの回答を評価することはできません。

評点者(scorer)
評価配信の中で、候補者からの回答の評価責任を持つ人または外部システム。評点者はオプションであり、例としては多くの項目評価は項目ごとに定義されている回答処理ルールに則り自動的に点数がつけられます。
A person or external system responsible for assessing the candidate's responses during assessment delivery. Scorers are optional, for example, many assessment items can be scored automatically using response processing rules defined in the item itself.

tutor

Someone involved in managing, directing or supporting the learning process for a learner but who is not subject to (the same) assessment.

candidate

The person being assessed by an assessment test or assessment item.

top
3. Structure of this Specification
The specification is spread over a number of documents:

Implementation Guide: A document that takes you through the data models by example. The best starting point for readers who are new to QTI and want to get an idea of what it can do.
Assessment Test, Section and Item Information Model: The reference guide to the main data model for assessment tests and items. The document provides detailed information about the model and specifies the requirements of delivery engines and authoring systems.
Metadata and Usage Data: A document that describes a profile of the IEEE Standard for Learning Object Metadata [LOM] data model suitable for use with assessment tests and items and a separate data model for representing usage data (i.e., item statistics). This document will be of particular interest to developers and managers of item banks and other content repositories, and to those who construct assessments from item banks.
Results Reporting: A reference guide to the data model for result reporting. The document provides detailed information about the model and specifies the associated requirements on delivery engines.
Integration Guide: A document that describes the relationship between this specification and other related specifications such as IMS Content Packaging [IMS_CP], IMS Simple Sequencing [IMS_SS] and IMS Learning Design [IMS_LD].
XML Binding: A document describing the way the data models have been bound to [XML].
Migration Guide: A document aimed at people familiar with version 1.x. It takes you through the main changes that have been made to the data model and includes an alphabetical listing of version 1 elements providing detailed information about how the same information is represented in version 2.
top
4. Conformance, Extensions, and Specification and Profile Maintenance
Because the QTI 2.1 specification is designed to accommodate a wide range of practices, conformance is defined in, and tested against, specific profiles. Such a profile can define which parts of the specification a community intends to support (items, tests, packages, results), and what specific features in each of those areas. In some cases, profiles can also include extensions to the specification, which are outlined in further detail below.

A certification of conformance against an existing profile is granted by passing a series of tests, submitting the results to IMS Global and agreeing to become part of the support community [QTI_APIP]. IMS records all certifications of conformance to current profiles on the public IMS certification website [IMS_CERT]. At the time conformance is certified, IMS issues a unique registration number designator for the product name and version for use in proposals. Buyers and users are invited to visit the certification website to find certified products and to log any issues with certified products.

Communities that are interested in defining their own profiles are encouraged to examine current profiles for appropriateness or for inspiration. Contact IMS Global for the possibilities of adopting, adapting or defining a profile of QTI to meet the requirements of your particular community.

Details about conformance related to both QTI and [APIP] are available on [ASSESS_PRIMER]. This page also lists the profiles that are currently available for conformance certification. One of these is the QTI Formative Entry profile, which captures the same assessment requirements represented in Common Cartridge v1.x (based on a profile of the QTI v1.2 specification). Interoperability with this profile was demonstrated by systems involved in the development of the v2.1 specification.

The IMS QTI/APIP Assessment APMG (Accredited Profile Management Group) is responsible for the ongoing maintenance of the QTI and APIP specifications, as well as those profiles that are available for conformance testing.

4.1 Extension Mechanisms
QTI 2.1 can be extended in two ways: with Custom Interactions and Custom Operators. Custom operators are a means of introducing more sophisticated processing of candidate's responses. This is particularly useful where the responses are likely to contain subject specific constructs such as computer code fragments or mathematical proofs. Further information and guidance on using custom operators is available in section 3.4.1 of the Implementation Guide of this specification.

Custom Interactions are a means of using interaction types that are not covered by the interaction types of the specification itself. These custom interactions trade a degree of interoperability for a wider range of user experiences. Because of the interoperability cost, care should be taken in defining such custom interaction types, since they may well be covered by a particular configuration of an already existing interactiontype. More information and best practice about sharing and running custom interactions is available at [INTERACT]. Work is underway to make types of custom interactions 'runnable', and therefore interoperable and sharable. More information will be made available at [INTERACT] in due course.

Custom operators and custom interactions can be shared by registering them at [QTI_INPUT]; already registered custom extensions can be viewed at [QTI_REG]. The [QTI_INPUT] form requires the submitter to specify the title of the submitted custom extension, a short description, a schema (XSD or DTD) that defines the structure of the custom item, and the name and organization of the author of the custom extension. The name and affiliation of the submitter is automatically recorded. Optionally, the submission can include images, long descriptions, the name of a tool that implements the custom extension, and a website URL where more information about the tool and/or the custom extension is available.

Once the vocabulary is submitted, the process proceeds as follows:

A submission confirmation email is returned to the submitter of the custom extension;
The custom extension is validated with respect to the registration process, i.e., technical correctness, valid submission XSD or DTD and naming (this is to ensure that name clashes do not occur). If a valid custom extension has been received it will be listed on [QTI_REG]. Validation is undertaken by the IMS Global core staff;
The corresponding validation response is returned to the submitter of the custom extension;
If and when there is a next revision of the QTI specification, the IMS QTI/APIP Assessment APMG (Accredited Profile Management Group) will automatically take the custom extension into consideration for inclusion in the specification. In that case, the workgroup will contact the original submitter.
In the cases where a vocabulary is rejected, then an explanation will be given for the rejection. An amended vocabulary can be resubmitted and this will be treated without prejudice.

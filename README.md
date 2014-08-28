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

Table of Contents
1. Question and Test Interoperability
1.1. History of this Specification
1.2. Scope
2. Specification Use Cases
2.1. Use Case Actors
3. Structure of this Specification
4. 4. Conformance, Extensions, and Specification and Profile Maintenance
4.1 Extension Mechanisms
5. Recent Changes
6. References

1. 質問とテスト相互運用方法

質問とテスト相互運用方法 (QTI)仕様書は、質問(評価項目)とテスト（評価テスト）のデータおよびその結果報告を説明するデータモデルを記述しています。
この仕様によって、項目、テストおよび結果をオーサリングツール、項目保管場所、テスト構成ツール、学習システムや評価配信システム間で交換可能になります。
データモデルは抽象的に記述され、UMLを使用して幅広いデータモデルツールとプログラミング言語を結合しますが、システム間の相互変換に、業界標準であるXML (eXtensible Markup Language)を結合に用いることができ、この結合方法を強く推奨します。 
IMS質問とテスト相互運用方法 (QTI)仕様書は、明確に定義された拡張ポイント規定を通して、相互運用性および革新の両方を支援します。これらの拡張ポイントは、特別なあるいは独自データを隠蔽するのに利用することができ、並びの項目を直接表現することができます。

1.1 仕様書の歴史

最初のV0.5仕様は、1999年3月の議論のために発売されたと11月に、それは、その年2000年2月と5月の最終仕様としてパブリックドラフトとしてリリースされたIMS質問＆テスト相互運用性V1.0を開発することで合意した。仕様は、IMS QTIの6000のコピーを超えて、その年の2月では2001年3月と2002年1月に、二度延長され、更新された1.xの仕様IMSのウェブサイトからダウンロードされていた。

それ以来、の多くの問題が実装者によって提起されたとQTIプロジェクトチームによってレビュー。それらの多くは、仕様のバージョン1.2.1を定義し、それらは下位互換性がないであろう仕様への変更を必要に応じて問題の一部では、この方法で対処することができなかった2003年3月に発売された補遺で扱ったまたはそれらが解決するのに大規模な明確化や仕様の大幅な延長を必要とする、より基本的な問題を明らかにしているため。

QTI仕様が最初に考案されたので、IMS仕様の幅広さは、成長し、コンテンツパッケージングの作業、シンプルシーケンシングや、最近ラーニングデザインは、クロス仕様の見直しの必要性を作成しています。このレビューは2003年の間に起こったとQTIに影響する調和の問題の数が確認された。9月、その年にはプロジェクト憲章は、から収集問題の両方に対処することが合意された1.xのと調和の問題をしてQTI V2.0を起草する。仕事を管理可能との結果がいくつかの制限が推奨される作業の範囲に置かれた最も早い機会にコミュニティに戻されたことを確実にするために。そのため、仕様のQTI V2.0リリースは、個人のみassessmentItemに集中し、セクションやテストへの項目の集計や結果の報告を扱っ仕様の部分を更新しませんでした。このQTI 2.1のリリースからアップデートを完了するの1.xに 2.xの QTI仕様のものの残りの部分を置き換えることによって。

1.1. History of this Specification
An initial V0.5 specification was released for discussion in March 1999 and in November it was agreed to develop IMS Question & Test Interoperability v1.0 which was released as a public draft in February 2000 and as a final specification in May that year. The specification was extended and updated twice, in March 2001 and January 2002. By February of that year in excess of 6000 copies of the IMS QTI 1.x specifications had been downloaded from the IMS web-site.

Since then, a number of issues of have been raised by implementers and reviewed by the QTI project team. Many of them were dealt with in an addendum, which defined version 1.2.1 of the specification and was released in March 2003. Some of the issues could not be dealt with this way as they required changes to the specification that would not be backwardly compatible or because they uncovered more fundamental issues that would require extensive clarification or significant extension of the specification to resolve.

Since the QTI specification was first conceived, the breadth of IMS specifications has grown and work on Content Packaging, Simple Sequencing and most recently Learning Design created the need for a cross-specification review. This review took place during 2003 and a number of harmonization issues affecting QTI were identified. In September that year a project charter was agreed to address both the collected issues from 1.x and the harmonization issues and to draft QTI V2.0. In order to make the work manageable and ensure that results were returned to the community at the earliest opportunity some restrictions were placed on the scope of the recommended work. Therefore, the QTI V2.0 release of the specification concentrated only on the individual assessmentItem and did not update those parts of the specification that dealt with the aggregation of items into sections and tests or the reporting of results. This QTI 2.1 release completes the update from 1.x to 2.x by replacing those remaining parts of the QTI specification.

1.2. Scope
The IMS QTI work specifically relates to content providers (that is, question and test authors and publishers), developers of authoring and content management tools, assessment delivery systems and learning systems. The data model for representing question-based content is suitable for targeting users in learning, education and training across all age ranges and national contexts.

top
2. Specification Use Cases
QTI is designed to facilitate interoperability between a number of systems that are described here in relation to the actors that use them.

Specifically, QTI is designed to:

Provide a well documented content format for storing and exchanging items independent of the authoring tool used to create them.
Support the deployment of item banks across a wide range of learning and assessment delivery systems.
Provide a well documented content format for storing and exchanging tests independent of the test construction tool used to create them.
Support the deployment of items, item banks and tests from diverse sources in a single learning or assessment delivery system.
Provide systems with the ability to report test results in a consistent manner.
components

Figure 2.1 The Role of Assessment Tests and Assessment Items.

authoringTool

A system used by an author for creating or modifying an assessment item.

itemBank

A system for collecting and managing collections of assessment items.

testConstructionTool

A system for assembling tests from individual items.

assessmentDeliverySystem

A system for managing the delivery of assessments to candidates. The system contains a delivery engine for delivering the items to the candidates and scores the responses automatically (where applicable) or by distributing them to scorers.

learningSystem

A system that enables or directs learners in learning activities, possibly coordinated with a tutor. For the purposes of this specification a learner exposed to an assessment item as part of an interaction with a learning system (i.e., through formative assessment) is still described as a candidate as no formal distinction between formative and summative assessment is made. A learning system is also considered to contain a delivery engine though the administration and security model is likely to be very different from that employed by an assessmentDeliverySystem.

2.1. Use Case Actors
The set of roles identified in this specification have been reduced to a small set of abstract actors for simplicity. Typically roles in real learning and assessment systems are more complex but, for the purposes of this specification, it is assumed that they can be generalized by one or more of the roles defined here.

author

The author of an assessment item. In simple situations an item may have a single author, in more complex situations an item may go through a creation and quality control process involving many people. In this specification we identify all of these people with the role of author. An author is concerned with the content of an item, which distinguishes them from the role of an itemBankManager. An author interacts with an item through an authoringTool.

itemBankManager

An actor with responsibility for managing a collection of assessment items with an itemBank.

testConstructor

The role of test constructor is to create tests (test forms) from individual items. The items are typically drawn from an item bank.

proctor

A person charged with overseeing the delivery of an assessment. Often referred to as an invigilator. For the purposes of this specification a proctor is anyone (other than the candidate) who is involved in the delivery process but who does not have a role in assessing the candidate's responses.

scorer

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

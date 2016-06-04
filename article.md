---
title: 'Disclosing funding sources for open access publication fees: the Open APC
  initiative'
author:
- Najko Jahn, Bielefeld University Library, Bielefeld University (TIB) - German National
  Library of Science and Technology, Hannover, Germany
- <a href="http://orcid.org/0000-0002-5111-2788">Marco Tullney</a>, Technische Informationsbibliothek
date: "7 April 2016"
output:
  pdf_document:
    fig_caption: yes
    keep_tex: yes
    template: peerj.sty
  html_document:
    fig_caption: yes
    force_captions: yes
    number_sections: no
    theme: readable
bibliography: literatur.bib
csl: frontiers.csl
abstract: Publication fees in open access publishing hold a prominent place on the
  agenda of researchers, policy-makers, and academic publishers. This paper contributes
  to the evolving empirical basis on open access funding. It describes the Open APC
  initiative, in which German universities and research organizations share their
  expenditures for publication fees. As method, the initiative uses existing open
  data tools to aggregate and disseminate institutional spending on open access publication
  fees. In total, 29 German research organizations self-reported funding of 6,279
  open access journal articles, which amounted to 8,039,339 €. The average payment
  for each article was 1,280 €, and the median payment 1,209 €. Our data-set comprises
  only 53 articles in hybrid journals. With an indexing coverage of 99 %, the findings
  reveal that the DOI agency Crossref provides both comprehensive bibliographic coverage
  of the funded open access journal literature and disambiguated names of journal
  titles and publishing houses. We show that authority control of these bibliographic
  information is particularly relevant for the comparative study of the economical
  effects of open access publishing.
---



# Introduction{.unnumbered}

## General Background{.unnumbered}

<!-- Publication fees, often paid by funders or universities, are a widely discussed business model for open access journals. Yet, how and to what extent these activities are effective in terms of the number of supported research articles and associated costs remains under debate. This study contributes to a growing empirical base about institutional spending on open access publication fees. More specifically, it uses self-reported cost data from German universities and research organisations to examine how much they spent, and how the so funded open access journal articles were distributed over publishers and journal titles using bibliographic information from Crossref. Such an approach extends methods and improves data collection activities for researchers and practitioners alike, as well as contribute to a better understanding of factors affecting the analysis of publication fees in open access publishing. -->

The rise of open access journals matches the increasing relevance of publication fees in academic publishing [@Davis_2011; @Laakso_2012; @Pinfield_Review_2015]. To cover these fees, also referred to as article-processing charges (APC), authors tend to make use of funding that grant agencies or academic institutions provide [@Suber_2012]. Yet, how and to what extent these research support activities are effective in terms of the number of supported articles and associated costs remains under debate. 

One reason why the study on how much was being spent is in most cases difficult is that total publication fee spending is fragmented across the budgets of grant agencies, research institutions, and libraries, or, if support is limited, are taken from personal budgets. Asking 9,645 authors from various disciplines how they financed publication fees, a comprehensive survey in 2010 revealed that the majority of the respondents had access to research funding or institutional support to cover these charges. By contrast, 12 % paid publication fees individually [@soap]. These findings are consistent with that of other studies, adding that sources of funding mostly exists in higher income countries, mainly to support research articles in the bio- and physical sciences [@Solomon_2011]. Personal budgets, on the other hand, are likely used to cover low price publication fees [@Solomon_2011; @Bj_rk_2015]. 

Another key problem in this regard is that funding for open access journals using publication fees lacks transparency because the parties involved - authors, universities, funders, publishers - neither release information on who pays for what nor the costs of publishing [@Bj_rk_learned_2014], a situation similar to the lack of transparency regarding journal subscriptions [@Lawson_Meghreblian_2015]. Empirical studies examining publication fees so far obtained price estimates by surveying authors [@soap], or from journal websites. Using the latter method, two studies investigating journals across a broad range of disciplines calculated similar price averages that ranged between 904 $ [@Solomon_2012] and 923 $ [@Walters_2011], as well as considerable price variances across journals and publishers. Accordingly, @Solomon_2012 suggested to cluster fully open access journal using publication fees into several groups. In descending order, these are high-impact journals, followed by biomedicine journals from commercial publishers, large multi-disciplinary journals, and mid-price journals from commercial publishers covering a large spectrum of disciplines. Lower priced journals were published by academic societies and by publishers from low-income countries. 

Nevertheless, it remains unclear which factors contribute to pricing in academic publishing. Generally, these might include article processing, impact, rejection rates, management and investment, and profit margins [@Van_Noorden_2013]. While fixed prices for individual articles are common, agreements between publishers and institutions can lead to discounts, and publishers sometimes waive publication fees for authors from low-income countries [@BJ_RK_2012; @Lawson_waiver_2015]. Other factors leading to variable pricing schemes include submission or page charges [@BJ_RK_2012]. 

Hybrid journals substantially add to this complexity of open access funding [@Kingsley_2014; @Pinfield_2015]. These journals, allowing articles to be published immediately as open access after a charge was paid, rely both on subscriptions and publication fees as revenue sources. Although the uptake of open access through hybrid journals was described as lower and more expensive compared to that of fully open access journals [@Solomon_2012; @Bj_rk_learned_2014], this model has gained attention through recent science policies, notably because of open access policies from the UK [@Pinfield_Review_2015]. 

To address these problems of fragmented spending on publication fees and of in-transparency about what was being paid, some European research funders and research performing institutions have recently begun to disclose their payment for publication as open data. To our knowledge, the first research funders providing such data were the Wellcome Trust [@wellcome_apc_12] and the Austrian Science Fund FWF [@fwf_apc_13]. The not-for-profit company Jisc followed by collecting data from higher-education institutions in the UK [@Lawson_data_2015]. Disclosed as publicly available spreadsheets, these data-sets self-report what was being spent along with bibliographic information, including title, journal and publisher, and a persistent identifier to the publisher's version. Curatorial efforts focused on the disambiguation of publisher and journal titles as well as on detecting duplicates and persistent identifiers to the full text [@Neylon_2014; @woodward_2014]. Parts of Jisc's cost data was examined by @Pinfield_2015. Although the average spending on publication fees remained stable across the universities, they found large price variances, as well as a varying number of articles UK universities supported between 2007 - 2014, confirming earlier studies that collected price information from journal websites.

<!-- This complex situation of fee-based open access publishing creates difficulties for researchers and practitioners alike. Some European initiatives have therefore begun to collect and disclose their expenditures on open access journal articles as open data. To our knowledge, the first research funders providing such data were the Wellcome Trust [@fwf_apc_13] and the Austrian Science Fund FWF [@wellcome_apc_12]. The not-for-profit company Jisc followed by collecting data from higher-education institutions in the UK [@Lawson_data_2015]. Disclosed as publicly available spreadsheets, these data-sets self-report payments made along with bibliographic information, including title, journal and publisher, and a persistent identifier to the publisher's version, and a link to a deposit in a subject repository. Curatorial efforts focused on the disambiguation of publisher and journal titles as well as on detecting duplicates. In the case of the Wellcome Trust, crowd-sourcing data cleaning activities through a Google spreadsheet in combination with checks against bibliographic sources massively improved the spending data (see comments in @wellcome_apc).-->


## Central funding for publication fees in Germany{.unnumbered}

This paper focuses on how much German universities and research organisation spent on open access publication fees. In Germany, the Deutsche Forschungsgemeinschaft (DFG), the largest German research funder, has strongly influenced how universities manage institutional support for publication fees.[^3] Before the DFG started to pay for centrally funded publication fees on a pro rata basis through its "Open-Access Publishing" program in 2011, and similar to the situation described in Canada [@Hampson_2014] or the UK [@PINFIELD_2012], only few central funds existed [@eppelin_2012]. Because the DFG has enforced a set of criteria grantees have to comply with, similar implementations for supporting open access publishing across German universities exists [@Fournier_2013]. These criteria exclude sponsoring of articles in hybrid journals, and the funding of articles whose publication fee exceeds 2,000 € (excluding value added tax)[^3]. Grantees agree not only to reimburse the bills on behalf of the researchers they support, but also to look for ways to improve the handling of those financial transactions. This includes central invoicing schemes, and related agreements between university libraries and publishers, leading to discounts for the authors [@Fournier_2013]. 

Research institutes organised in the Fraunhofer-Gesellschaft, Helmholtz-Gemeinschaft, Leibniz-Gemeinschaft, and Max-Planck-Gesellschaft are not eligible for this DFG funding program. But in response, some organizations have adopted similar processes to support authors. The Max-Planck-Gesellschaft operates their long-lasting open access activities, including handling spending and publisher agreements centrally, through the Max Planck Digital Library [@Schimmer_2013; @Sikora_2015], while the Leibniz-Gemeinschaft set up a dedicated open access fund in 2016.

The evolving institutional support structures to cover open access publication fees has led to calls for an unified approach towards supporting open access journal publishing in Germany. The Allianz der Wissenschaftsorganisationen[^10c], a science policy board representing all major research organisations in Germany, marked price transparency as one way to sustain an "adequate open access publication system" [@allianz]. Reflecting Austrian and UK initiatives to share institutional spending on open access publication fees as open data, as well as professional discussions on open access publishing, Bielefeld University Library began to openly share its payment of publication fees in May 2014. After engaging with the working group "Electronic Publishing" of the Deutsche Initiative für Netzwerkinformation (DINI)[^11] other German institutions joined under the umbrella of the Open APC initiative soon after.

## Research question{.unnumbered}

The aim of the study was to examine how much German universities and research organisations spent on open access publication fees until 2015. Using self-reported cost data from the Open APC initiative, the analysis focused on the amount that was being spent on publication fees, and compared these expenditure with data from related Austrian and UK initiatives, both in terms of size and the proportion of articles being published in fully and hybrid open access journals. We also asked how thoroughly self-reported articles were indexed in Crossref, a DOI minting agency for scholarly literature, and analysed how institutional spending per articles was distributed over publishers and journal titles. 

# Methods and Materials{.unnumbered}

We analysed self-reported cost data released by the Open APC initiative on May 13, 2016[^24] to assess institutional spending on open access publication fees in Germany. In addition to administrative data about the amount paid per article including value added tax, the reporting institution, and the year of invoicing, we used information about whether an article was published in a fully or hybrid open access journal as well as the recorded DOI from the data-set.

We fetched bibliographic metadata for each article from Crossref on May 19, 2016, on the basis of the reported DOIs. Although the Open APC initiative gathered metadata representing publishers and journals from Crossref as well, this information was retrieved at the time when the participating institutions submitted their expenses. The Open APC initiative kept track of the date when these data-sets were submitted with Git, a version control system, increasingly used for enabling reproducible research [@Ram_2013], and made this information available via GitHub to be transparent over time. However, during these data collection activities Crossref had regularly updated metadata to represent ongoing mergers of publishing houses. A prominent example in this regard was the merger of the two large publishing houses Springer Business + Media and Nature Publishing Group announced on May 6, 2015, that operated as Springer Nature at the time of our study. To reflect these dynamics in academic publishing, we decided to retrieve updated metadata from Crossref for the whole Open APC data-set instead of re-using the historical publisher and journal information contained in the Open APC data-set.

As a client, we used the R package rcrossref [@rcrossref], developed and maintained by the rOpenSci initiative[^6], to access Crossref's REST API[^25]. We requested the XML-based format `application/vnd.crossref.unixsd+xml` in which full and abbreviated journal titles as well as the ISSN media types, the International Standard Serial Number used to identify journals, were distinguished. It also contained normalised publisher information, thus avoiding confusion about naming of publishing houses other studies were faced with when working with self-reported data [@woodward_2014]. In cases where no bibliographic information could be obtained, we used the Open APC values. Because Crossref was not the only registration agency for DOIs, but also the agencies DataCite and Medra minted DOIs for scholarly work, we furthermore obtained the DOI agency for each article with the help of the rcrossref client.

Data collection also involved obtaining cost data from related open data initiatives. To compare self-reported spending on open access journal articles by Germany universities and research organisations with that of other initiatives, we consulted the openly available data-sets from the the Austrian Science Fund FWF [@fwf_apc_14; @fwf_apc_15], Jisc [@jisc_14; @jisc_15] and the Wellcome Trust [@wellcome_apc_13_14; @wellcome_apc_14_15]. For analysis, we obtained the overall publication fee spending on both fully and hybrid open access journal articles. In the case of FWF, we gathered the cost information from the accompanying spending reports. We used the spreadsheet data to calculate Wellcome Trust's and Jisc's spending, and converted the prices from GBP to € in accordance with the average € foreign exchange reference rates provided by the European Central Bank. Our comparison between the open data initiatives focussed on the last two years 2014 and 2015. Because Wellcome Trust's spending was reported for the financial periods 2013 - 2014 and 2014 - 2015, we referred to the average exchange rates of the full two-year period as we could not determine the actual invoicing dates from the data. We excluded articles from the analysis for which either cost information or journal type was missing. In the case of Jisc's 2014 data [@jisc_14], for instance, we excluded spending on 2,812 publications that amounted to 4.861.772 € from the analysis because no publication type was given in the data-set.

The data collection methods of the Open APC initiative and those of the other initiatives differed in some aspects. For instance, whereas the DOI was a mandatory element in the Open APC data template that the participating institutions were required to report, in the Wellcome Trust data a publication identifier was added as part of the automated compliance checks. Our first screening of the data-sets revealed that some articles lacked a DOI. For this reason, and as our main focus was institutional funding for publication fees in Germany, we decided to only compare German APC spending with that reported by other initiatives. We did not compare the distribution of spending over publishers and journal titles, or the indexing coverage in Crossref. 

# Results{.unnumbered}





## Cost Data{.unnumbered}



After excluding payments being made for non-journal articles, as well as articles invoiced in 2016, we retrieved 7,417 open access journal articles 30 German universities and research institutions financially supported between 2005 and 2015. As illustrated in Figure 1, payments made for open access journal articles grew over the years. While one institution supported 5 articles in 2005, the majority shared their expenditure from 2013 onwards. With 1,999 articles, the year 2015 was best represented in our data-set. However, the data-set contained 27 institutions that contributed their cost data for 2015 at the time of this analysis, suggesting a time lag between payments made and reporting these spending to the Open APC initiative.

**Figure 1: Growth of Open APC Initiative**








Among all articles, fees amounted to 9,627,537 € including VAT, the average payment was 1,298 € and the median value 1,231 € . Figure 2 presents the distribution of institutional spending on publications. We observed that 6,996 (94%) of the publication fees were paid in accordance with the DFG price cap of 2,000 €. Most payment on publications ranged between 1,000 - 1,250 €. 

**Figure 2: Distribution of institutional spending on publication fees by German research organisations**

**Figure 3: Institutional spending on publication fees by German research organisations per year**

Figure 3 presents the large price variations. Publication fees that were paid by the German universities and research organisations ranged between 40 € and 7,419 €  (SD 486). However, the average price paid varied somewhat during the period 2011 and 2015 (1239 - 1423 €). Average publication fee spending per article in Germany was 1,298 (Median = 1,231 €, SD = 486 €).



The number of APC payments per institutions varied considerably (see Table 1). With 2,856 reported articles, the Max Planck Society contributed 39 % of the overall submissions. By contrast, the universities of technology, TU Clausthal, TU Dortmund TU Ilmenau that recently begun to set up support structures for fee-based open access journal articles, self-reported low numbers of payments.

**Table 1: Institutional spending on open access publications (in €)**



## Comparision of related cost data-sets

Table 2 compares Open APC spending data with that of the Austrian FWF, as well as with Jisc's and Wellcome Trust's expenditure. Prices were converted according to the average Euro exchange rate of the examined periods, and gathered for both fully and hybrid open access journals. The comparison reveals that the Open APC initiative lacked cost information about hybrid journals, whereas the related Austrian and UK open data initiatives could report a large share of spending on these journals between 2014 and 2015. This situation presumably reflected the importance of the DFG as funding source for publication fees in Germany. The DFG funding policy excluded support for publications in hybrid journals. Over the years 2005 – 2015, 3 out of 30 German universities and research institutions reported 60 hybrid journal articles to the Open APC initiative, representing 0.81 % of the overall supported article volume. In terms of the number of supported articles and the amount being spent on publication fees, by contrast, the Open APC data-set provided the most comprehensive price information for fully open access journals compared to what the Austrian and UK initiatives had reported.



Comparison of average prices suggests that publishing in hybrid journal was more expensive than in fully open access journals. Price differentials between these two categories were also reported earlier, indicating that prices for fully open access journals were typically lower [@Solomon_2012; @Pinfield_2015]. In 2014 and 2015, the mean price for fully open access journals calculated from all data-sets was below the DFG price cap of 2,000 €.

## Crossref indexing{.unnumbered}



To identify publication fee spending on the article-level, as well as to gather bibliographic metadata, DOIs were a mandatory part of the Open APC initiative's data collection activities. The participating institutions reported DOIs for 7,373 out of 7,417 articles. Using these DOIs, we retrieved additional metadata from Crossref for 7,346 publications, representing 99 % of the total article volume. Articles for which no metadata could be obtained, were registered with the DOI agency DataCite (10 articles) or Medra (two articles). For eight articles, our parser could not gather the XML resource, although these publications were registered with Crossref at the time of our study. Seven DOIs reported to the Open APC initiative did not resolve.


## Cost data by publisher and journal{.unnumbered}




We used the DOI to automatically fetch publisher and journal names for each article from the Crossref REST API. Table 4 shows the top ten publishers in terms of payments made that represented 92 % of the overall spending on publication fees. In total, payments were made to 139 publishing houses. In comparison with data from the UK, some open access publishers have a greater share on total spending. @Pinfield_2015, for instance, reported remarkably lower numbers for the open access publishers MPDI AG, Copernicus GmbH, and Hindawi Publishing.

**Table 2: Publication fees paid per publisher (in €)**



Most of publication fee spending in Germany was on articles published in Springer Nature journals, most likely profiting from the merge with the open access publisher BioMed Central in 2008, and that between the well-established publishers Springer Science + Business Media and Nature Publishing Group in 2015. Using the Crossref-Member-ID instead of the publisher name, we were able to differentiate between journals formely published by Springer Science + Business Media and Nature Publishing Group. In terms of articles, the majority of payments made were for publications in journals formerly associated with Springer Science + Business Media. Springer Science + Business Media journals accounted for 2,027 articles, representing 94% of the overall Springer Nature article volume in the Open APC data, and 92 % in terms of the amount being spent. Median publication fee spending slightly differed between Springer Science + Business Media (1,355 €) and Nature Publishing (1,386 €). However, price variation was higher for Nature Publishing journals (SD = 848€) compared with that of the former Springer Science + Business Media titles (SD = 313 €). 

In contrast to Springer Nature, other well-established publishing houses such as Elsevier and Wiley-Blackwell rank lower in our analysis. Table 2, furthermore, illustrates the price variations across and within publishers, which confirms earlier findings [@Solomon_2012; @Pinfield_2015].

**Table 3: Publication fees paid per journal (in €)**



Prices also varied within single journals. Based on the number of articles paid for, Table 3 illustrates the top ten out of 732 journals. Payments to these journals represent 45 % of the overall expenditure. In the case of Atmospheric Chemistry and Physics Discussions, the large price range can be explained by the fact that this journal charges per page and also takes the submission's file format into consideration.

# Discussion{.unnumbered}

In Germany, institutional spending on open access publication fees has increased over the years, confirming the general trend of publication fees in academic publishing [@Davis_2011; @Laakso_2012; @Pinfield_Review_2015]. With a share of 99%, the majority of open access articles German institutions reported to the Open APC initiative were published in fully open access journals. This presumably reflects the DFG funding policy which excludes the support of articles published in hybrid open access journals. The DFG has been financially supporting the implementation of central publication funds at more than 30 German universities since 2009. However, in reviewing self-reported cost data from funders or countries that also support hybrid open access journals or open access books, we revealed smaller proportions of payments in favour of articles in fully open access journals. Because open access publication fee spending is fragmented, we cannot answer whether German researchers avoided opting for open access when publishing in hybrid journals or used other budgets to pay publication fees required to make their work open access through these kind of journals. 

In our study, Crossref thoroughly indexed open access journal articles in the Open APC data-set. We could gather metadata representing publisher and journal titles for 99 % articles, and successfully merged these information with the Open APC cost data. Using metadata from Crossref, therefore, reduces the extensive validation work of bibliographic information provided that the reporting of the DOI along with the expenses is made mandatory. Drawing on Crossref would also increase the comparability of cost data for future negotiations with publishers on open access agreements, and the open access spending between open data initiatives that apply the same reporting standards, as its metadata represent the dynamic landscape of academic publishing in terms of ongoing mergers of publishing houses or name changes.

Another advantage of self-reported data-sets on the article-level to disclose spending on open access publication fees is that they enable researchers and practitioners alike to study in which open access journals researchers from one institution actually publish, and to compare these findings with that of other universities or research organizations. For instance, our study revealed that the size of publication fee spending differed among the institutions with the Max Planck Society accounting for almost 39 % of the overall articles. Many universities and research organization reported remarkably lower number of supported open access articles to the Open APC initiative. Using self-reported data, therefore, contributes to the understanding about how much and to what extent spending on open access publishing varies on the institutional level. This is particularly relevant given the increasingly important role open access publishing plays in recent negotiations between German universities and research organizations forming consortia on the one side and publishers on the other about financing scholarly publishing in future [@allianz].

This study is limited in some respects. One is that we cannot assess whether publishers and journals granted publication fee discounts seeing that the Open APC initiative does not track this kind of information. However, the large price ranges of particular journals suggests that varying pricing schemes were in place. Adding to this complexity, it is likely that some institutions only paid parts of the publication fee. Take for instance the journal Nature Communication. Charges reported in our sample ranged between 2000 €, the DFG price cap, and 4.403 €. Such co-payments that involve several budgets were a proposed strategy to sustain publication funds at German universities [@Fournier_2013]. In another case, one university included its charges for participating in the German SCOAP consortia and presumably divided the sum by the articles published in SCOAP journals. In this national consortia, managed by the German National Library of Science and Technology, payments were not directly made per article. Instead, subscription costs between a participating library and a publisher were reconciled, and the reduction transferred to the consortia to finance publications in SCOAP journals. 

It must also be noted that reporting to the Open APC initiative is voluntary. Therefore, not all institutions in Germany that provide central funding of publication fees contribute cost data to this initiative. In a qualitative survey, asking why German institutions are reluctant to share their cost data through the Open APC initiative, one institution feared that increase in transparency would allow publishers to adjust prices in their favour. Others pointed out that the workload to produce such a data-set could be too extensive [@deppe_2015]. As no registry of institutional open access funds or similar support structures exists, we cannot assess the number of non-participants in Germany.

Our analysis on how institutional spending per articles was distributed over publishers and journal titles shows that open access publishing is diverse and concentrated at the same time. While we were able to identify 139 individual publishing houses that were supported by the German universities and research organizations, the distribution is highly skewed. 92 % of open access publication fee spending went to ten publishers, confirming a general high concentration of few publishers in current academic publishing. However, our study could not confirm that publications in open access journals owned by traditional publishing houses account for most of the spending on publication fees. Rather, open access publishers such as Public Library of Science (PloS), Copernicus GmbH or MPDI AG rank higher in our study than in the analyses of cost data in the UK. 

This study finally confirms the leading role of "mega-journals" in open access publishing, including the multidisciplinary PLOS ONE and the journals New Journal of Physics, Atmospheric Chemistry and Physics Discussions and Frontiers in Psychology, all of which publish contributions from all branches of their respective discipline. In general, an estimated 14 out of more than 10,000 journals registered in DOAJ in 2015 accounted for up to 15–20 % of all articles published in full open access journals [@Bj_rk_2015].

# Conclusion{.unnumbered}

<!-- The purpose of the Open APC initiative is to gain better insight on spending for open access. The main operational idea—to make data submission easy by building upon existing data and by using popular open tools and data bases—has proven to be a feasible approach and to scale well. Starting with a few institutions, the integration of further data contributors has not been a problem. While we use article metadata reported by publishers to Crossref, we think it's best to collect information on how much has been spent at the sources: the institutions paying for APCs. We look forward to more data contributors to the initiative and to adapt this scheme to new analyses, additional data, or international sources. The Open APC initiative can serve as an example of the value that open data, open source software, and the knowledge and skills of tech-savvy librarians add to modern tasks of libraries.-->



# Acknowledgment{.unnumbered}

We thank Andrea Hacker and Ada-Charlotte Regelmann for valuable comments on the first draft of this paper. We also thank Christoph Broschinski, Vitali Peil, and Dirk Pieper, the members of the DINI working group "Electronic publishing", and all data contributors[^20] of the Open APC initiative.


# References{.unnumbered}


[^1]: Comprehensive list of business and revenue models of open access journals: <http://oad.simmons.edu/oadwiki/OA_journal_business_models>

[^2]: <https://github.com/openapc/openapc-de>

[^2a]: Project summary available at <https://github.com/OpenAPC/openapc-de>. The initiative is now supported by the INTACT project: http://www.intact-project.org/.

[^2b]: However, it should be noted that the administrative costs of processing invoices for a large number of articles are not measured in this project.

[^3]: Guidelines for the funding program can be found here: <http://www.dfg.de/formulare/12_20/>

[^3a]: We are sure that some universities with DFG-funded publication funds pay for APCs higher than 2,000 €. They have to make sure they don't use the funder's money for these articles, and this maybe explains why some institutions are reluctant to report on these APCs. Scatter plots of all APC payments show that there are only very few APCs over 2,000 €.



[^5]: CrossRed: Text and Data Mining for Researchers: <http://tdmsupport.crossref.org/researchers/>

[^6]: rOpenSci: <https://ropensci.org/>

[^7]: Europe PubMed Central RESTful Web Service: <https://europepmc.org/RestfulWebService>

[^8]: Thomson Reuters Article Match Retrieval Service: <http://wokinfo.com/directlinks/amrfaq/>

[^9]: <https://doaj.org/faq#metadata>

[^10]: <http://rmarkdown.rstudio.com/>

[^10c]: <http://www.dfg.de/en/dfg_profile/alliance/index.html>

[^11]: <http://dini.de/english/ag0/e-pub0/>

[^12]: <http://openapc.github.io>

[^13]: <https://jekyllrb.com/>

[^13a]: <http://opendatacommons.org/licenses/odbl/1-0/>

[^14]: <https://lists.uni-bielefeld.de/mailman2/cgi/unibi/listinfo/open-apc>

[^15]: <https://github.com/OpenAPC/openapc-de/wiki>

[^16]: <https://github.com/OpenAPC/openapc-de/issues>

[^16a]: The data is openly available on GitHub. The following analysis is based on version 2.1.13 of the dataset, available at <https://github.com/OpenAPC/openapc-de/tree/v2.1.13>.

[^17]: <http://contributor-covenant.org/>

[^18]: <https://github.com/CrossRef/rest-api-doc/blob/master/rest_api.md>

[^19]: We would like to thank Martin Fenner for pointing this out to us. See also the Crossref API documentation <https://github.com/CrossRef/rest-api-doc/blob/master/rest_api.md>

[^20]: <https://github.com/OpenAPC/openapc-de#contributors>

[^22]: <http://dx.doi.org/10.4119/UNIBI/UB.2014.18>

[^23]: <https://github.com/OpenAPC/openapc-de/wiki/Handreichung-Dateneingabe>

[^24]: https://github.com/OpenAPC/openapc-de/tree/v2.4.3

[^25]: <https://github.com/CrossRef/rest-api-doc/blob/master/rest_api.md>

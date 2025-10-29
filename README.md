# Open Accept: Metadata
Open Accept (OAc) is the place where you can find facts regarding paper acceptance rates in global Computer Science conferences.
OAc's goal is to provide vital insights into the CS research community. Since acceptance rates and other important statistics are scattered all over the internet, community collaborations are of great importance in achiving this goal.

## Where I can find the data?
- **Social media platforms**. Many researchers share their papers on social media platforms. They may also attach the notification email, which discloses the acceptance rate, in the post.
- **Conference websites**. A lot of conferences choose to make acceptance rates public directly on their websites. (for instance, [CHI 2025 Paper Outcomes Report](https://chi2025.acm.org/chi-2025-papers-track-post-pc-outcomes-report/))
- **Conference proceddings**. Conference proceedings may also disclose the acceptance rate. The most typical way is to mention the acceptance rate in "preface" or the "chairs note" section. (for example, [ICDE 2024 Proceddings, "A Message from the Chairs"](https://ieeexplore.ieee.org/document/10598037))
- **On-site slides**. Chairs may also share the acceptance rate in the slides. This may requires in-person attendance. But in some cases, photos of the slides may be shared on social media.

## How can I contribute?
It's easy to contribute to OAc. Please fork the repository, make changes, and submit a pull request. Please make sure that your contribution comply with the data format. The general template is as follows:
```json
{
  "name": "Conference name abbreviation (e.g., AAAI)",
  "full_name": "Conference full name",
  "website": "Website URL",
  "dblp": "DBLP URL",
  "yearly_data": [
    { "year": 2025, "submitted": 12957, "accepted": 3032 },
    { "year": 2024, "submitted": 9862, "accepted": 2342 },
    { "year": 2023, "submitted": 8777, "accepted": 1721 },
    { "year": 2022, "submitted": 9020, "accepted": 1349 }
  ],
  "sources":[
    "https://urls.here"
  ]
}
```
If the conference has a secondary strack (currently, OAc only takes *short papers*, *ACL Findings*, and *KDD ADL* into statistics), please refer to the template below:
```json
{
  "name": "Conference name abbreviation (e.g., AAAI)",
  "full_name": "Conference full name",
  "website": "Website URL",
  "dblp": "DBLP URL",
  "yearly_data": [
    { "year": 2025, "submitted": 12957, "accepted": 3032 },
    { "year": 2024, "submitted": 9862, "accepted": 2342 },
    { "year": 2023, "submitted": 8777, "accepted": 1721 },
    { "year": 2022, "submitted": 9020, "accepted": 1349 }
  ],
  "second_track": "Findings",
  "second_track_yearly_data": [
    {"year": 2024, "accepted": 976, "submitted": 4407},
    {"year": 2023, "accepted": 901, "submitted": 4864},
    {"year": 2022, "accepted": 331, "submitted": 3378},
    {"year": 2021, "accepted": 361, "submitted": 3350}
  ]
  "sources":[
    "https://urls.here"
  ]
}
```

## Policy on adding new conferences
When adding a new conference, please make sure that the conference is listed in CCF's Recommended International Conferences and Journals Catalog or Core Ranking.

Considering the audience reach and the difficulty of data maintenance, OAc primarily includes conferences listed in [CCF's Recommended International Conferences and Journals Catalog](https://www.ccf.org.cn/Academic_Evaluation/By_category/) and [Core Ranking](https://www.core.edu.au/conference-portal). You can add new conferences that are not listed in the above two lists, but the core maintainers may need more time to discuss and review your pull request. It is advised to contain a short justification in your pull request.
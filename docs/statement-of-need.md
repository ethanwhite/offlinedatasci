# Statement of Need

Data, data science tools, and data science educational materials are predominantly distributed online.
As a result, access to data science tools and skills is not homogeneously distributed. The [median percentage of population with internet access across all countries is only
60.1%](https://www.cia.gov/the-world-factbook/field/internet-users/).
This includes varying degrees of consistency ranging from continuously to only once every few months.
In the US, [degree of internet access is associated with race and ethnicity, geography, and income](https://aspe.hhs.gov/reports/low-income-internet-access).
Low-income US households are less likely to have access to broadband and
more likely to have no internet access at all.
Although the increase in internet access worldwide is undeniable,
the rate at which access increases and the quality of that access
remains unequally distributed.

Most online data science tools and teaching materials assume a stable internet connection to download data, install software, and view teaching materials while learning or working.
This need for regular internet access can be mitigated by obtaining the necessary data, software, and lesson materials when and where internet access is available.
Once these materials are downloaded, much of the associated training and data science work can be accomplished without internet access.
However, the knowledge necessary to accomplish this is often not available to people starting out with learning data science skills.
This makes limited internet access particularly challenging in teaching environments,
where students often learn how to download and install data science tools during classes and workshops.
Workshops may have to be run in venues without reliable internet access and many of the students may not have sufficient, affordable internet access prior to the workshop,
leading to problems in acquiring hundreds of megabytes worth of software applications and their dependencies for workshop participants.
Simplifying the downloading and offline use of data science components that have internet requirements could ameliorate some of the challenges that students and data scientists face due to unequal accessibility to the internet.

The offlinedatasci package is part of a growing set of tools and instructional materials developed by CarpentriesOffline to facilitate teaching and practicing data science in internet-limited environments.
The larger ecosystem allows local computers and low power devices such as the Raspberry Pi to be used as isolated servers that provide a wireless network to workshop participants, so that they can acquire the necessary materials during workshops even when there is no internet access.

The *offlinedatasci* package automates downloading or updating a bank of materials for running workshops or practicing data science offline, by providing:

1) open source statistical and graphing software (R and Python)
2) integrated development environments (IDEs) for working with this software (RStudio
and Jupyter)
3) up-to-date mirrors of the package repositories used to install data science packages (CRAN, PyPI)
4) online lesson materials configured for local viewing (currently a selection of [Carpentries](https://carpentries.org) workshop lessons with their respective practice data sets).

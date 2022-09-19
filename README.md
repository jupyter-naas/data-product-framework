![Naas.ai - Open Source Data Platform](assets/project_logo.png)

# Naas - Data Product Template

Naas is a low-code open source data platform that allows anyone touching data (business analysts, scientists and engineers) to create powerful data products combining automation, analytics and AI from the comfort of their [Jupyter Notebooks](https://jupyter.org/).

With its open source distribution model, Naas enforces visible source code, versionning and allow you to create custom logics. Naas's low-code based approach makes it highly versatile, enabling you to built almost everything.

The platform is structured around 3 low-code layers: 
- Templates enable the user to create automated data jobs in minutes, and are the building blocks of data products
- Drivers act as connectors to push and/or pull data from databases, APIs, and Machine Learning algorithms and more
- Features transform Jupyter in a production ready environment with scheduling, asset sharing, and notifications

Try Naas for free using -- Naas cloud -- a stable environment, in your browser.

## How Does This Repository Works?

This repository is a boilerplate for anyone who wish to develop a data product using Naas.

It is structured as follows: 
- `/assets` folder to store any PNG, JPG, GIF, CSV, diagrams, slides related to the documentation of the product
- `/inputs` folder to store the parameters and any other files needed (data, referential) to run  used in the /models folder
- `/models` folder to store any files that transform inputs into outputs (notebook, python, SQL files)
- `/outputs` folder to store all the files that would be exposed outside of the Naas server
- `/utils` folder to store all common functions used accross files
- `/requiremets.txt` file to list out all the packages and dependencies
- `/settings.ipynb` file to run the product on a Naas server 
- `/update.ipynb` file to pull this repository again



## About This Data Product

![Naas.ai Email](assets/mail.gif)

This Data Product Template simulates a very simple use case where a stock market data analyst needs to send out report every day at 9 AM to his manager. The email contains:
- the current stock value of a specific stock (TSLA in this example),
- the variation vs the previous day but also projected stock value using basic ML algorithms
- a chart in PNG inserted in the body of the email 
- a call-to-action to open view the chart dynamically using HTML inside the browser
- the source data in excel for further exploration 

### Built With

* YahooFinance data
* Jupyter Notebooks
* Naas

## Documentation

### Prerequisites

* Create an account on [naas.ai](https://www.naas.ai/free-forever)

### Installation

Follow the [settings.ipynb](settings.ipynb) notebook steps.

## Roadmap

- [x] V0 - simple version with only one ticker 
- [ ] V1 - multiple tickers (portfolio) input and an dashboard app available on the web
- [ ] V2 - multiple KPIs analysis to arbitrate investment between different tickers


## Support

If you have problems or questions please open an issue, we will then try to help you asap:

[Open an issue](https://github.com/jupyter-naas/data-product-template/issues).


## Contributing

Contributions are welcomed.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star.

1. Create an account on [naas.ai](https://www.naas.ai/free-forever)
2. Clone [the repository](https://github.com/jupyter-naas/data-product-template) on your engine 
2. Create your Feature Branch
3. Commit your Changes
4. Push to the Branch
5. Open a Pull Request


## Product Owners

* [Florent Ravenel](https://www.linkedin.com/in/florent-ravenel/) - florent@naas.ai
* [Jeremy Ravenel](https://www.linkedin.com/in/ACoAAAJHE7sB5OxuKHuzguZ9L6lfDHqw--cdnJg/) - jeremy@naas.ai


## Acknowledgments

* [Awesome Notebooks](https://github.com/jupyter-naas/awesome-notebooks)
* [Naas Drivers](https://github.com/jupyter-naas/drivers)
* [Naas](https://github.com/jupyter-naas/naas)


## Legal

This project is licensed under AGPL-3.0
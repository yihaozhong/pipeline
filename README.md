# pipeline

## Ingest
### Working with json
?json.dump


### Specifying the schema
StructField
{'items': [{'brand': 'Huggies',
            'model': 'newborn',
            'price': 6.8,
            'currency': 'EUR',            
            'quantity': 40,
            'date': '2019-02-01',
            'countrycode': 'DE'            
            },
           {…}]
### API

## Transformation
### Remove, fillna, select, rename, groupby, clean
Five very common data transformations involved in applying business logic you will encounter are: Filtering data. It allows us to focus only on the data that are useful for a particular analysis.

Selecting and renaming columns allows us to focus only on fields of interest and possibly renaming them to make their meaning more clear.

Grouping rows by a particular field and then aggregating some metrics, like the mean price and the number of samples. If you have sales data, for example, you can group it by country, and calculate the total revenue per country.

Joining DataFrames by linking them through certain fields allows you to add more attributes to records in your data.

## Testing

### Unit test (pytest, unittest, doctest, nose)
Core task: assert or raise

### Automating test
Git -> configure hooks

### CI/CD
integrated with the main branch regularly. To instruct it to retrieve the code from some company’s internal version control system and run the pytest module

circleCI looks for .circleci/config.yml

To install package dependencies, you should be looking for a requirements.txt file (or a Pipfile), which is in the repo. So you should download it before installing the dependencies.

Code -> code test -> artifacts

## Scheduling

### cron
`*/15 9-17 ** 1-3, 5 log_my activity`

### Airflow
create and visualize complex workflows, monitor and log workflows and scales horizontally. 

#### Directed Acyclic Graph (DAG)
node is an action and instance. edge is the direction

#### Dependencies between operators
task1.set_downstream(task2)

task3.set_upstream(task2)

task1 >> task2

task3 << task2
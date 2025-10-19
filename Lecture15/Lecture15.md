# Lecture 15

---

## Data Gathering

1. CSV Files
2. JSON/SQL Data
3. Fetch from API
4. Web Scraping

### CSV Files

- CSV stands for Comma Separated Values.
- TSV files are available too and are known as Tab Separated Values.
- Multiple parameters are present to handle files and its structure.

### Pandas Commands to handle CSV Files

- Opening a local csv file
  `df = pd.read_csv('aug_train.csv')`

- Sep Parameter
  `pd.read_csv('movie_titles_metadata.tsv',sep='\t',names=['sno','name','release_year','rating','votes','genres'])`

- Index_col parameter
  `pd.read_csv('aug_train.csv',index_col='enrollee_id')`

- Header parameter
  `pd.read_csv('test.csv',header=1)`

- use_cols parameter
  `pd.read_csv('aug_train.csv',usecols=['enrollee_id','gender','education_level'])`

- Squeeze parameters
  `pd.read_csv('aug_train.csv',usecols=['gender'],squeeze=True)`

- Skiprows/nrows Parameter
  `pd.read_csv('aug_train.csv',nrows=100)`

- Encoding Parameter
  `pd.read_csv('zomato.csv',encoding='latin-1')`

- Skip bad lines
  `pd.read_csv('BX-Books.csv', sep=';', encoding="latin-1",error_bad_lines=False)`

- dtypes Parameter
  `pd.read_csv('aug_train.csv',dtype={'target':int}).info()`

- Handling Dates
  `pd.read_csv('IPL Matches 2008-2020.csv',parse_dates=['date']).info()`

- Convertors
  `pd.read_csv('IPL Matches 2008-2020.csv',converters={'team1':rename})`

- na_values Parameter
  `pd.read_csv('aug_train.csv',na_values=['Male',])`

- Loading a huge dataset in chunks
  `dfs = pd.read_csv('aug_train.csv',chunksize=5000)`
  `for chunks in dfs:`
  `    print(chunk.shape)`

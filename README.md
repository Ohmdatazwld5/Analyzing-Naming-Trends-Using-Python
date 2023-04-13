# Analyzing-Naming-Trends-Using-Python
Popular baby names data provided by Social Security Administration (SSA) of United States

For each year of birth YYYY after 1879, we created a comma-delimited file called yobYYYY.txt. Each record in the individual annual files has the format "name,sex,number," 
where name is 2 to 15 characters, sex is M (male) or F (female) and "number" is the number of occurrences of the name.
Each file is sorted first on sex and then on number of occurrences in descending order

*visualize the number of male and female babies born in a particular year with the help of
pandas.DataFrame.plot, then Analyse baby names by sorting out all birth counts.*

*analyse baby names by sorting out top 100 birth counts and group them by names to find
out popular baby names*

# Analysing Name Trends

boy_name = top_100_names[top_100_names.Sex=='M']
girl_name = top_100_names[top_100_names.Sex=='F']

total_birth = top_100_names.pivot_table('Sex', index='Year', columns='Name', aggfunc= 'sum')
boy_name.head()

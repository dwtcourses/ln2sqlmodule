# ln2sqlmodule

This is an adoption of the awesome [ln2sql](https://github.com/FerreroJeremy/ln2sql) by [Jérémy Ferrero](https://github.com/FerreroJeremy) as a python module so that people can easily use it to create some awesome things !

# INSTALLATION

- Download, unzip and place in your project directory
- `import ln2sqlmodule`

# USAGE

- **ln2sqlmodule.getSql(query,sqlDump)**
	returns SQL query from natural language query

	    Parameters :
			query      :    query in natural language
			sqlDump    :    path to sql dump file           
		
		returns : 
			SQL query string

		Example:
			ln2sqlmodule.getSql("get name of all emp","./emp.sql")
			-> SELECT name FROM  emp

- **ln2sqlmodule.getSql_like(query,sqlDump)**
	returns SQL query from natural language with **LIKE** with **%** in **WHERE** clause

	    Parameters :
			query      :    query in natural language
			sqlDump    :    path to sql dump file           
		
		returns : 
			SQL query string with LIKE

		Example:
			ln2sqlmodule.getSql("all data for emp where name is rupinder","./emp.sql")
			-> SELECT * FROM  emp WHERE name LIKE '%rupinder%'

			ln2sqlmodule.getSql("all data for emp where name is 'abc xyz'","./emp.sql")
			-> SELECT * FROM  emp WHERE name LIKE '%abc%xyz'

 
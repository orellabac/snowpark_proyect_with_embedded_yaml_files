Example Project Loading different yml files dynamically



Using this project:

Run:

```
snow snowpark build

```

You will get an output like: `Build done. Artifact path: /Users/mrojas/Downloads/parameterized_snowpark/app.zip`

Then run

```

snow snowpark deploy --connection mobilize --replace
```

This will display:

```
+----------------------------------------------------------------------------------+
| object                                                     | type      | status  |
|------------------------------------------------------------+-----------+---------|
| SNOWPARK_TESTDB.PUBLIC.run_commands(yaml_file_path string) | procedure | created |
+----------------------------------------------------------------------------------+

```

And to run it use:

```

snow snowpark execute procedure "run_commands('sample1.yml')" --connection conn1
```

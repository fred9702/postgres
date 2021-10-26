<b>pgBench</b> is a simple program for running benchmark tests on PostgreSQL. It runs the same sequence of SQL commands over and over.

To get started, run <i>docker-compose up</i>.

When you run pgBench, it creates the following tables:

pgbench_accounts   
pgbench_branches   
pgbench_history   
pgbench_tellers    

Check in psql with \d in the db you ran pgbench against. In this case it is tembo_db.

Typical output looks like:

<code>
    transaction type: builtin: TPC-B 

    scaling factor: 10

    query mode: simple

    number of clients: 10

    number of threads: 1

    number of transactions per client: 1000

    number of transactions actually processed: 10000/10000

    tps = 85.184871 (including connections establishing)

    tps = 85.296346 (excluding connections establishing)

</code>

The tps value fluctuates depending on the scale factor at which you benchmarked the Postgres db and the hardware on which the postgres db runs.

For a cool guide on how to tune postgres by changing the "shared_buffer" values, go here: https://www.cloudbees.com/blog/tuning-postgresql-with-pgbench
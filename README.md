

**Cassandra**

Create keyspace

create keyspace if not exists ehr_db with replication = { 'class':'SimpleStrategy', 'replication_factor':1};

Patient Table

create table if not exists patients (
mrn_id text primary key,
document text,
created_at timestamp,
updated_at timestamp
);


Appointment Table

create table if not exists appointments (
id UUID primary key,
mrn_id text,
practitioner_id text,
document text,
created_at timestamp,
updated_at timestamp
);

Practitioner Table

create table if not exists practitioners (
id text primary key,
document text,
created_at timestamp,
updated_at timestamp
);

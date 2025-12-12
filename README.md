

**Cassandra**

Create keyspace: 
create keyspace if not exists ehr_db with replication = { 'class':'SimpleStrategy', 'replication_factor':1};

Create Patient Table: 
create table if not exists patients (
mrn_id text primary key,
document text,
created_at timestamp,
updated_at timestamp
);


Create Appointment Table
create table if not exists appointments (
id UUID primary key,
mrn_id text,
practitionerId text,
document text,
created_at timestamp,
updated_at timestamp
);

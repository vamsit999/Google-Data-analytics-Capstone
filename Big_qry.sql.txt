First create tables for all months data for 2020, 2021,2022  in big query.
I had to limit data to first 1000 rows as there is a data limitations in big query.

Create 

Create table course5-analyze-data.capstone_proj.divvy_tripdata_All_2020 as
select * from (
(SELECT * FROM `course5-analyze-data.capstone_proj.202006-divvy-tripdata` LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202007-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202008-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202009-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202010-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202011-divvy-tripdata`  LIMIT 1000)
)
;

Create table course5-analyze-data.capstone_proj.divvy_tripdata_All_2021 as
select * from (
(SELECT * FROM `course5-analyze-data.capstone_proj.202101-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202102-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202103-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202104-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202105-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202106-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202107-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202108-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202109-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202110-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202111-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202112-divvy-tripdata`  LIMIT 1000)
);


Create table course5-analyze-data.capstone_proj.divvy_tripdata_All_2022 as
select * from (
(SELECT * FROM `course5-analyze-data.capstone_proj.202201-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202202-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202203-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202204-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202205-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202206-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202207-divvy-tripdata`  LIMIT 1000)
union all
(SELECT * FROM `course5-analyze-data.capstone_proj.202208-divvy-tripdata`  LIMIT 1000)
);

Create table course5-analyze-data.capstone_proj.divvy_tripdata_All_2020_21_22 as
select * from (
(select * from course5-analyze-data.capstone_proj.divvy_tripdata_All_2020 LIMIT 757)
union all
(select * from course5-analyze-data.capstone_proj.divvy_tripdata_All_2021 LIMIT 875)
union all
(select * from course5-analyze-data.capstone_proj.divvy_tripdata_All_2022 LIMIT 1000)
)

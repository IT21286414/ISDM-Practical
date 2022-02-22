# ISDM-Practical



/*lab 2-page 3*/
SELECT Mname, NoOfCredits from Module;

SELECT Sname FROM Student where Sname LIKE 'A%';

Select sname, dob from Student where dob < '1996/01/01';

SELECT sname from Student where Address  LIKE '%colombo%';

SELECT sname FROM Student WHERE sname Like 'K%' AND CID = 'DS';

SELECT sname FROM Student WHERE CID = 'DS' OR CID = 'IT';

/*lab 2-page 4*/
SELECT * FROM Student ORDER BY NIC DESC;

SELECT * FROM Student ORDER BY sname ASC, CID DESC ; 

/*lab 3 -page 4*/
SELECT COUNT(SID) FROM Student ;

SELECT COUNT(CID) FROM Course ;

SELECT COUNT(CID) as 'Total num' FROM Course;

SELECT COUNT(Mcode) as '3 Credits' FROM Module where NoOfCredits = '3';

SELECT SUM(C_fee) as 'Total Fee' FROM Course;

SELECT MAX(C_fee) as 'highest Fee' FROM Course;

SELECT MIN(C_fee) as 'min Fee' FROM Course;

SELECT AVG(C_fee) as 'AVG Fee' FROM Course;


/*lab 4 */

select * from student

Select CID, count(SID) from Student group by CID; 

select * from module

select * from offers

select * from Course

/* lab 4 - page 3 */

SELECT M_Description , sum(NoOfCredits) AS 'Total Credits' from  Module group by M_Description

SELECT CID, COUNT(SID) AS 'Number Of Students' from Student Group by CID

SELECT CID , Accadamic_year , COUNT(Accadamic_year) from Offers group by CID, Accadamic_year
order by  Accadamic_year asc, CID asc

SELECT CID, Count(Mcode) from Offers where Semester = '2' group by CID 

SELECT CID, Count(Mcode) from Offers where Semester = '2' group by CID order by CID Asc



/* lab 5 - page 4*/ 
SELECT * from Module
SELECT * from Course
SELECT * from Offers
SELECT * from Student

SELECT CID, COUNT(SID) from Student Group by CID Having COunt(SID) < 10; 

SELECT CID, Count(Mcode) from Offers Group by CID HAVING count(Mcode) > 3 order by COUNT(Mcode) asc

SELECT CID, Accadamic_year, count(Mcode) from Offers group by CID, Accadamic_year having Count(Mcode) < 10;

SELECT CID from Offers where Accadamic_year = 'Y3' group by CID having count(Mcode) > 2;


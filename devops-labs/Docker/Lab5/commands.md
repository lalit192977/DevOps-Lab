# Docker Lab 5 – Commands Reference

## Directory Preparation and Exploration

cd /root
ls

text

## Inspect Dockerfile for MySQL

cat Dockerfile-mysql
cat Dockerfile-mysql | grep ENTRYPOINT

text

## Inspect Dockerfile for WordPress

cat Dockerfile-wordpress | grep CMD
cat Dockerfile-wordpress # To review ENTRYPOINT and CMD, get full startup logic

text

## Inspect Dockerfile for Ubuntu

cat Dockerfile-ubuntu | grep CMD

text

## Build and Run Custom Ubuntu Image

docker build -t my-ubuntu -f Dockerfile-ubuntu .
docker run -d my-ubuntu sleep 1000

text
undefined

📄 lab-tasks.md

text
# Docker Lab 5 – Task Breakdown

---

## Task 1: List Files in /root Directory
**Commands:**

cd /root
ls

text
**Screenshot:** `01_root_ls.png`

---

## Task 2: Inspect MySQL Dockerfile for ENTRYPOINT
**Commands:**

cat Dockerfile-mysql
cat Dockerfile-mysql | grep ENTRYPOINT

text
**Screenshot:** `02_cat_dockerfile_mysql.png`, `03_entrypoint_mysql.png`

---

## Task 3: Inspect WordPress Dockerfile for CMD and ENTRYPOINT
**Commands:**

cat Dockerfile-wordpress | grep CMD
cat Dockerfile-wordpress # Reveals both ENTRYPOINT and CMD to determine startup behavior

text
**Screenshot:** `04_cmd_wordpress.png`, `05_cat_dockerfile_wordpress.png`

---

## Task 4: Inspect Ubuntu Dockerfile for CMD
**Command:**

cat Dockerfile-ubuntu | grep CMD

text
**Screenshot:** `06_cmd_ubuntu.png`

---

## Task 5: Build Custom Ubuntu Image & Run It
**Commands:**

docker build -t my-ubuntu -f Dockerfile-ubuntu .
docker run -d my-ubuntu sleep 1000

text
**Screenshots:** `07_build_my_ubuntu.png`, `08_run_my_ubuntu.png`

---

## Task 6: Discussion – ENTRYPOINT vs CMD

ENTRYPOINT sets the main command for the container that is always executed unless replaced with `--entrypoint` at run time.  
CMD provides default arguments or commands for ENTRYPOINT, which you can override during `docker run`.

- For MySQL and WordPress images, ENTRYPOINT and CMD may be combined; final container command = ENTRYPOINT + CMD (unless overridden).
- For custom Ubuntu, we replace CMD by passing `sleep 1000` at run time — demonstrating CMD's override flexibility[1][2][3][4][5][6][7][8][9].

---

## Lab Summary
You inspected and compared startup commands of images, understood the relationship between ENTRYPOINT and CMD, and built/run a custom Ubuntu image with an overridden command.
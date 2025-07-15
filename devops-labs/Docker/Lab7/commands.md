# Docker Lab 7 – Commands Reference

## Step 1: Run MySQL Container with Default Volume

docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 mysql

text

## Step 2: Verify Running Container

docker ps

text

## Step 3: Run SQL Data Initialization Script

sh get-data.sh

text

## Step 4: Explore Volume Directory in Host

ps
docker ps -a

cd /var/lib/docker
cd volumes
ls

cd 7878ce68399c107c2d5a02d0db18ff9459c2d0f6eade028c27962ae1c5cb6b04
cd _data
ls
cd mysql

text

## Step 5: Attach Existing Volume to New Container

docker run -d --name mysql-db -v 7878ce68399c107c2d5a02d0db18ff9459c2d0f6eade028c27962ae1c5cb6b04:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=db_pass123 mysql
docker ps

cd /root
ls
sh get-data.sh

text

## Step 6: Run MySQL using Host Path `/opt/data`

docker run -d --name mysql-db -v /opt/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=db_pass123 mysql

text
undefined

📄 lab-tasks.md

text
# Docker Lab 7 – Task Breakdown

---

## Task 1: Run MySQL Container with Environment Variable

docker run -d --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 mysql

text

🖼 Screenshot: `01_run_mysql_simple.png`

---

## Task 2: List Running Containers

docker ps

text

🖼 Screenshot: `02_docker_ps_running.png`

---

## Task 3: Run Initialization Script (`get-data.sh`)

sh get-data.sh

text

✅ Loads test tables into MySQL instance.

🖼 Screenshot: `03_sh_get_data_initial.png`

---

## Task 4: Investigate Host Volume Paths

cd /var/lib/docker/volumes
ls
cd <volume-id>/_data/mysql

text

✅ Check that volume contains MySQL database files

🖼 Screenshot: `04_docker_ps_a.png`, `05_var_lib_docker_volumes.png`, `06_volume_ls_nested.png`, `07_data_folder_inside_volume.png`

---

## Task 5: Mount Existing Volume and Repeat Script

docker run -d --name mysql-db
-v <volume-id>:/var/lib/mysql
-e MYSQL_ROOT_PASSWORD=db_pass123 mysql

sh get-data.sh

text

🖼 Screenshot: `08_mount_existing_volume.png`, `09_recheck_mysql_data.png`, `10_get_data_again.png`

---

## Task 6: Use Absolute Path (`/opt/data`) for Persistent Volume

docker run -d --name mysql-db
-v /opt/data:/var/lib/mysql
-e MYSQL_ROOT_PASSWORD=db_pass123 mysql

text

✅ External bind-mount used instead of anonymous/internal volume.

🖼 Screenshot: `11_run_with_named_volume.png`
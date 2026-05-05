# File name: cs4_solution.py

# ---------------- TASK 1: Basic File Reading ----------------

file = open("CS4.txt", "r")

content = file.read()
lines = content.split("\n")

print("Total number of lines:", len(lines))
print("\nFirst 2 lines:")
print(lines[0])
print(lines[1])

print("\nLast 2 lines:")
print(lines[-2])
print(lines[-1])

file.close()


# ---------------- TASK 2: Log Classification ----------------

file = open("CS4.txt", "r")
lines = file.readlines()

log_count = {"INFO": 0, "WARNING": 0, "ERROR": 0}

for line in lines:
    if "INFO" in line:
        log_count["INFO"] += 1
    elif "WARNING" in line:
        log_count["WARNING"] += 1
    elif "ERROR" in line:
        log_count["ERROR"] += 1

print("\nLog Counts:", log_count)

file.close()


# ---------------- TASK 3: Write Filtered Files ----------------

info_file = open("info_logs.txt", "w")
warning_file = open("warning_logs.txt", "w")
error_file = open("error_logs.txt", "w")

for line in lines:
    if "INFO" in line:
        info_file.write(line)
    elif "WARNING" in line:
        warning_file.write(line)
    elif "ERROR" in line:
        error_file.write(line)

info_file.close()
warning_file.close()
error_file.close()

print("\nFiltered files created successfully!")


# ---------------- TASK 4: Search Feature ----------------

keyword = input("\nEnter keyword to search (INFO/WARNING/ERROR): ")

file = open("CS4.txt", "r")
lines = file.readlines()

result_file = open("search_result.txt", "w")

print("\nMatching lines:")

for line in lines:
    if keyword in line:
        print(line.strip())
        result_file.write(line)

file.close()
result_file.close()


# ---------------- TASK 5: File Pointer Operations ----------------

file = open("CS4.txt", "r")

print("\nFirst 50 characters:")
print(file.read(50))

# Move to beginning
file.seek(0)
print("\nAfter seek(0):")
print(file.read(50))

# Move to middle
file.seek(0)
data = file.read()
middle = len(data) // 2
file.seek(middle)
print("\nFrom middle:")
print(file.read(50))

# Move to last 100 characters
file.seek(0)
file.seek(len(data) - 100)
print("\nLast 100 characters:")
print(file.read(100))

file.close()

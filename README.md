import datetim
import os

def create_daily_log():
    today = datetime.date.today().strftime("%Y-%m-%d")
    folder = "logs"
    
    if not os.path.exists(folder):
        os.makedirs(folder)

    file_path = os.path.join(folder, f"{today}.txt")

    with open(file_path, "w") as file:
        file.write(f"Daily log created for {today}.\n")
        file.write("Status: Script executed successfully.")

    print(f"Log file created: {file_path}")

if __name__ == "__main__":
    create_daily_log()

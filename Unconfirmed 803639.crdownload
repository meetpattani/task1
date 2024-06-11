import os
import shutil

root_dir = '/path/to/directory'

extension_folders = {
    'images': ['jpg', 'jpeg', 'png', 'gif'],
    'documents': ['docx', 'doc', 'pdf', 'txt'],
    'videos': ['mp4', 'avi', 'ov'],
    'audio': ['mp3', 'wav', 'ogg'],
    'archives': ['zip', 'rar', 'tar', 'gz']
}

for folder in extension_folders.keys():
    folder_path = os.path.join(root_dir, folder)
    if not os.path.exists(folder_path):
        os.makedirs(folder_path)

for filename in os.listdir(root_dir):
    file_ext = os.path.splitext(filename)[1][1:].lower()

    for folder, extensions in extension_folders.items():
        if file_ext in extensions:
            folder_path = os.path.join(root_dir, folder)
            shutil.move(os.path.join(root_dir, filename), folder_path)
            print(f"Moved {filename} to {folder_path}")
            break
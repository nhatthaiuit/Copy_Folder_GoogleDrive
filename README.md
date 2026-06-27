🚀 Superfast Google Drive Copier (A to B) on Google Colab
This tool helps you automatically copy all data from a shared Drive folder (Source) to your personal Google Drive (Destination) directly through Google's servers.

✨ Key Features
Lightning-fast speed: Data is transferred directly between Google's servers (Server-to-Server), reaching speeds of several GBs per minute.

Zero personal bandwidth usage: The copying process uses absolutely no local internet bandwidth or hard drive space.

Preserves folder structure: Say goodbye to Google automatically splitting large folders into messy 2.0GB .zip files with broken directory trees and scrambled file names.

Smart error handling: Automatically skips files with restricted download permissions or access errors without crashing the entire process.

🛠 Step-by-Step Guide
Step 1: Initialization

Upload this .ipynb source file to Google Colab.

Run the first Code cell (Authentication) by clicking the Play (▶) button.

A popup will appear. Sign in with your Google account and grant Colab permission to access your Google Drive. Wait for the ✅ Xác thực thành công! (Authentication successful) message.

Step 2: Get Folder Links

Your Drive (Destination): Create an empty folder in your Drive, open it, and copy the URL from your browser's address bar.

Shared Drive (Source): Open the shared folder you want to copy and copy its URL from the address bar.

Step 3: Start Copying

Run the second Code cell (Input).

Paste the two copied links into their respective input fields.

Click the ▶ Khởi chạy Copy (Start Copy) button.

Keep the browser tab open and your computer awake until the tool prints ✅ Done. Đã copy thành công... (Done. Successfully copied...).

⚠️ Important Notes (Must Read)
1. The "Shortcut" Issue
This tool cannot extract data directly from "Shortcuts" (folders/files with a curved arrow icon on them). If you input a link pointing to a Shortcut, it will only copy the shortcut link itself (a few KBs), not the actual videos/documents inside.
👉 Solution: Double-click the Shortcut in your Drive to navigate into the owner's actual root folder. Then, copy the URL of that root folder to use in the tool.

2. Red Error Messages (HTTPError 403 / cannotCopyFile)
You might see yellow/red warning lines printed during the process. This is completely normal and happens when:

You haven't been granted access to that specific file.

The owner has actively enabled the "Disable options to download, print, and copy" security setting.
👉 The system will automatically skip these locked files and continue copying the valid ones. The original folder owner will not receive any notifications.

3. Connection Drops
Google Colab will automatically disconnect if you close the browser tab, shut down your computer, let your PC go to Sleep, or if your internet disconnects for too long.
👉 If the process is interrupted, the tool cannot resume from where it left off. You must go to your Destination Drive, completely delete the partially copied folder, create a brand new empty folder, and run the tool from the beginning.

4. Storage Limits
Ensure your personal Google Drive has enough free space to accommodate all the incoming data. If your Destination Drive runs out of storage, the tool will throw an error and stop.

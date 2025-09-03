from pathlib import Path

# Define the story content
linux_story = """
# 🐧 A Simple Story to Understand Linux Directory Structure

## Once upon a time in Computerland...

There was a smart little penguin named Tux 🐧 who lived inside a magical world called **Linux**.

Tux's world was like a big house with many rooms. Each room had a special purpose. Let’s walk through Tux’s house and explore!

---

## 🏠 `/` - The Root of It All

This is the **main gate** of Tux's house. Everything starts from here. Just like the trunk of a tree, all other directories (rooms) branch out from this root.

---

## 🧰 `/bin` - Toolshed

Tux keeps his essential tools here – like a hammer, screwdriver, etc. In Linux, this folder has basic **commands** like `ls`, `cp`, and `mv`. Without this room, Tux can’t do much!

---

## 🧙‍♂️ `/sbin` - Secret Tools for Admins

Only Tux when wearing his **admin hat** (root user) can use the tools in this room. These are special system commands.

---

## 🧴 `/etc` - Rulebook Room

This room is full of **configuration files** – like rules, preferences, and secret recipes. Want to change how the house works? You go here.

---

## 🛋️ `/home` - Bedrooms

Each friend of Tux has their own room here. If Tux has a friend named **Alex**, Alex’s room is `/home/alex`. This is where they keep their personal files and treasures.

---

## 💽 `/var` - Storage for Notes and Logs

This room gets new stuff all the time – logs, emails, downloads. It's where Tux stores **variable data** that changes often.

---

## 📦 `/usr` - Guest House

This is a big guest house filled with useful things: apps, games, and libraries for all users. Tux invites his friends to use stuff from here.

---

## 🧪 `/lib` - Potion Cabinet

This room contains **libraries**, like magic potions, that help programs run. If Tux needs a spell (code) to make something work, he grabs it from here.

---

## ⚙️ `/dev` - Workshop

Here, Tux interacts with machines like printers and hard drives. Everything in this room is actually a file that represents a device.

---

## 🌌 `/proc` and `/sys` - The Brain and Nervous System

These rooms aren’t real—they’re more like **windows into the mind** of Linux. Tux looks in here to see how the system is feeling.

---

## 🧳 `/tmp` - Suitcase Room

Need to put something down just for a little while? Use this temporary room. But be quick—Tux cleans it out often!

---

## 🗑️ `/boot` - Booting Boots

Before Tux starts walking, he needs his boots. This room has the files Linux needs to start up.

---

## 🧼 `/opt` - Optional Room

Tux sometimes installs **extra apps** here that don’t come with the system.

---

## 👑 `/root` - Tux's Private Suite

This is Tux’s own room when he’s acting as the **root user**. Very private. Very powerful.

---

## The End... or the Beginning?

Now that you know Tux’s house, you can find your way around Linux too! 🗺️
"""

# Write to a markdown file
file_path = Path("linux_directory_structure_story.md")
file_path.write_text(linux_story)

print("✅ File 'linux_directory_structure_story.md' created successfully!")

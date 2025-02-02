---
title: Concepts
description: Explanations regarding the term of bulk & general storages
authors: 
    - Boold
---

# *This is bulk skits*

In this subchapter, contained key concepts of **General** & **Bulk** Storages.

???+ warning "Familiarize yourself with these required items"
    ![](img-bulk/booldBulkRequirements.png)  
    * Cell Workbench  
    * MEGA Bulk Item Storage Cell  
    * MEGA Decompression Module  
    * Compression Card  

## Where bulk terms is used
Before we went deeper, One might ask what is "bulk" and why we use it in storage, or where do we find it? moreover the importance of it to AE2 in this topic.  

Take a look at this mess:  

![](img-bulk/booldRandomMess.png){.center}  

From the image above, there's **random things** like building blocks, seeds, some saplings, and miscellaneous materials. We also notices that most of these items **does not exceed 3.000**. We'll call this as **Random Mess** for now.  

In contrast, from the image below, we can see that those items is **stored at a very big numbers** compared to the previous ones. Instead, we'll refer this as **Bulk Mess**  

![](img-bulk/booldBulkMess.png){.center}  

## General vs Bulk Storage 

All of those random bits and pieces of items previously typically stored insides what we call a **"General Storage"**. In a literal sense,
!!! quote "every dump & junks we insert to the network, will **eventually end up** in this type of storages."  

Just like the Random Mess we had before. Any other things then (generally) will be stored insides a **"Bulk Storage"**  
!!! note "A literal "storing items in bulks" !"

## Partition?

Just in case it's not obvious now, 'partitioning' cells is an **important aspect** when we talk about bulk storage. Imagine your creeper farm generating thousands upon thousands of gunpowder per minutes, this will clog up your 'general storage' quickly over time (you don't want your cells is filled up with gunpowder **only** didn't ya?).  

In this case, we **partition** a cell (generally the ones who can store a lot) and assigned it to a specific cell. **Priority System** in AE2 means you can tell items to go into a specific storage (or drives) **first**, before it goes into another storage.  

???+ tip "If you're looking on how to do partitions..."    
    Head over to [How To Partition A Cell](bulkhow.md/#partition)

???+ info "Items route in the network on General Storage vs Bulk Storage & Partitions in-between"
    ![](img-bulk/booldPriorityInsert.png)  
    The system works like this:   
    1. You insert the items into the network   
    2. The network now tried to "store" said items into the valid 'storage'  
    3. It checks the valid storage with the highest priority (in this case, Bulk storage, which **only accepts gunpowder**)  
    4. If it fails to store said items into the Bulk Storage (say, **a stick**), it checks again the next valid storage (eventually stored inside general storage)  
    > Thus gunpowder always get stored first inside bulk storage, and anything that isn't gunpowder stored inside general storage. It doesn't clog the system, and you can always dump more junks into the system. **This is why bulk storage is important**  
    ??? example "Example of this concept, visualized in an actual setup"
        ![](img-bulk/booldExamplePriority.png)  
        * Terminal in this case can also be represented as **Access Points**. Means it becomes a point where the network can accept items into it (hence the appearances of **Terminal** along with **Pattern Provider** & **Interface**)


For a better grasp of the differences between the two, take a look at this table:  

| **General Storage** <br> ![](img-bulk/itemCell.png) | **Bulk Storage** <br> ![](img-bulk/bulkCell.png) |
|:---:|:---:|
| Typically stores random things (miscellaneous items) | Typically stores specific items (mainly resources/mob drops/farm drops etc.) |
| Ex. Cobble walls, doors, fence, lantern, furnace | Ex. Iron ingots, spruce logs, diamonds, rotten flesh, wheat |
| Doesn't really wants "partition" | Partition is a must (at the very least, highly suggested) |
| Requires less works | Usually more steps to do |
| Good for dumping unorganized items | Good for optimizing your network contents |
| Tends to be used less per ME Drive | Tends to be used more per ME Drive |
| Identical with lower amount of items (less than 5k, etc.) | Identical with high number of items (thousands/millions/billions even!) |

??? tip "Did you know that?"
    Due to how storages in AE2 works (**Bytes & Types**) 20 item cells can store **1.260** types of items, but they stored less than 20 **Bulk Cells** ! This is also why we use the term General & Bulk storages.  

> Applied Energistics 2 | [CurseForge](https://legacy.curseforge.com/minecraft/mc-mods/applied-energistics-2)  
> MEGA Cells | [CurseForge](https://legacy.curseforge.com/minecraft/mc-mods/mega-cells)  
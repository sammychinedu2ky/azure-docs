---
title: Use labs for trainings - Azure Lab Services
description: This article describes how to use Azure DevTest Labs for creating labs on Azure for training scenarios.
ms.topic: how-to
ms.date: 01/04/2022
---

# Use labs for trainings

[!INCLUDE [preview note](./includes/lab-services-new-update-note.md)]

Azure Labs Services allows educators (teachers, professors, trainers, or teaching assistants, etc.) to quickly and easily create an online lab to provision pre-configured learning environments for the trainees. Each trainee would be able use identical and isolated environments for the training. Policies can be applied to ensure that the training environments are available to each trainee only when they need them and contain enough resources - such as virtual machines - required for the training.

![Lab](./media/classroom-labs-scenarios/classroom.png)

Labs meet the following requirements that are required to conduct training in any virtual environment:

- Trainees can quickly provision their training environments
- Every training machine should be identical
- Trainees can't see VMs created by other trainees
- Control cost by ensuring that trainees cannot get more VMs than they need for the training and also shutdown VMs when they are not using them
- Easily share the training lab with each trainee
- Reuse the training lab again and again

In this article, you learn about various Azure Lab Services features that can be used to meet the previously described training requirements and detailed steps that you can follow to set up a lab for training.  

## Create the lab plan as a lab plan administrator

The first step in using Azure Lab Services is to create a lab plan in the Azure portal. After a lab plan administrator creates the lab plan, the admin adds users who want to create labs to the **Lab Creator** role. The educators create labs with virtual machines for students to do exercises for the course they are teaching. For details, see [Create and manage lab plan](how-to-manage-lab-plans.md).

## Create and manage labs

An educator, who is a member of the Lab Creator role in a lab plan, can create one or more labs in the lab plan. You create and configure a template VM with all the required software for doing exercises in your course. You pick a ready-made image from the available images for creating a lab and then optionally customize it by installing the software required for the lab. For details, see [Create and manage labs](how-to-manage-labs.md).

## Set up and publish a template VM

A template in a lab is a base virtual machine image from which all users’ virtual machines are created. Set up the template VM so that it is configured with exactly what you want to provide to the training attendees. You can provide a name and description of the template that the lab users see. Then, you publish the template to make instances of the template VM available to your lab users. When you publish a template, Azure Lab Services creates VMs in the lab by using the template. The number of VMs created in this process is same as the maximum number of users allowed into the lab, which you can set in the usage policy of the lab. All virtual machines have the same configuration as the template. For details, see [Set up and publish template virtual machines](how-to-create-manage-template.md).

## Configure usage settings and policies

The lab creator can add or remove users to the lab, get registration link to send to lab users, set up policies such as setting individual quotas per user, update the number of VMs available in the lab, and more. For details, see [Configure usage settings and policies](how-to-configure-student-usage.md).

## Create and manage schedules

Schedules allow you to configure a lab such that VMs in the lab automatically start and shut down at a specified time. You can define a one-time schedule or a recurring schedule. For details, see [Create and manage schedules for labs](how-to-create-schedules.md).

## Use VMs in the lab

A student or training attendee registers to the lab, and connects to the VM to do exercises for the course. For details, see [How to access a lab](how-to-use-lab.md).

## Next steps

Start with creating a lab plan in labs by following instructions in the article: [Tutorial: Setup a lab plan with Azure Lab Services](tutorial-setup-lab-plan.md).

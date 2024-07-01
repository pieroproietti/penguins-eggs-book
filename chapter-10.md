# Chapter 10

# Testing the ISO

To test an ISO created with the `eggs` tool, you can follow
these general steps:

1.  Prepare a Testing Environment: Set up a virtual machine or a
    physical system where you can test the ISO. This can be done
    using virtualization software like VirtualBox or by booting the ISO
    on a separate machine.

Setting up a testing environment for your ISO can be done using a
virtual machine or a physical system. Here\'s how you can do it:

> 2.Virtual Machine Testing:

* Install a virtualization software, prefer KVM based, like `gnome-boxes`, `proxmox-ve`, etc, over proprietary `virtualbox` or `VMware`;

* Create a new virtual machine using the virtualization software.

* During the virtual machine creation process, configure the system
specifications such as CPU, memory, and storage based on your
requirements.

* When prompted to select an ISO or boot media, choose the ISO file
created with the "eggs" tool.

* Complete the virtual machine creation process and start the virtual machine.

* The virtual machine will boot from the ISO, allowing you to test the
operating system or software contained within the ISO.

> 3. Physical System Testing:

-   Prepare a separate computer or device where you can boot the
    ISO.

-   Create a bootable USB drive or burn the ISO to a DVD.

-   Insert the bootable USB or DVD into the target system.

-   Restart the system and access the boot menu or BIOS settings.

-   Choose the bootable USB or DVD as the primary boot device.

-   Save the settings and restart the system.

-   The system will boot from the ISO, allowing you to test the
    operating system or software contained within the ISO.

By using either of these methods, you can create a controlled
environment to test your ISO and ensure its functionality and
compatibility.

> 4. Boot the ISO: Start the virtual machine or the target system
> and boot from the ISO you created with the "eggs" tool.
> Ensure that the ISO is accessible during the boot process.
>
> 5. Test Installation: If the purpose of the ISO is to install an
> operating system, go through the installation process and verify that
> it completes successfully. Pay attention to any errors, warnings,
> or unexpected behavior during the installation.

## Testing the installation 

When testing the installation process of an ISO, follow these steps to
ensure it completes successfully:

1)  Start the system or virtual machine using the ISO as described in
    the previous steps.

2)  Follow the on-screen instructions to begin the installation
    process.

3)  Provide any required information, such as language preferences,
    keyboard layout, time zone, and user credentials.

4)  Pay attention to any error messages, warnings, or unexpected
    behavior during the installation. Note down any issues you
    encounter.

5)  Proceed through the installation process, selecting the desired
    installation options. This may include disk partitioning,
    software selection, and additional configurations.

6)  Monitor the progress of the installation and ensure that it
    completes without any errors or interruptions.

7)  Once the installation is finished, the system will prompt you to
    restart or boot into the newly installed operating system.

8)  After restarting or booting into the installed system, verify that
    it functions correctly. Check if essential features like
    networking, display, sound, and other hardware components are
    working as expected.

9)  Test basic functionality and run some applications to ensure they
    work properly.

10) Document any issues or bugs you encounter during the installation
    process and note any steps to reproduce them.

By carefully testing the installation process, you can identify and
address any issues or errors that may occur, ensuring that the
installation completes successfully and the operating system is
functional.

## Test Functionality

Test Functionality: Once the installation is complete, boot into the
installed system and test its functionality. Check if essential
features like networking, display, sound, and other hardware components
are working correctly. Run some basic applications to ensure they
function as expected. After the installation process is complete,
you can proceed to test the functionality of the installed system.
Here are the steps to follow:

1)  Restart or boot into the newly installed operating system.

2)  Check Network Connectivity:

    -   Ensure that the networking features are working correctly.

    -   Connect to the internet and verify if you can access websites or
        perform network-related tasks.

    -   Test both wired and wireless connections if applicable.

3)  Display and Graphics:

    -   Check if the display resolution is set correctly and matches the
        capabilities of your monitor.

    -   Verify that graphics and animations are rendered smoothly
        without any visual artifacts or glitches.

    -   Test playing videos or running graphics-intensive
        applications to ensure they function properly.

4)  Sound and Audio:

    -   Play audio files or videos with sound to confirm that the audio
        output is working as expected.

    -   Test different audio inputs and outputs (e.g.,
        speakers, headphones, microphone) if available.

5)  Hardware Compatibility:

    -   Test other hardware components such as printers, scanners,
        external storage devices, or any other peripherals that are
        relevant to your use case.

    -   Ensure that the system detects and functions with these hardware
        devices without any issues.

6)  Basic Application Testing:

    -   Run basic applications such as web browsers, text editors, media
        players, and office productivity software.

    -   Verify that these applications launch correctly and perform
        their intended functions without errors.

7)  Perform Additional Testing:

    -   If there are specific applications or functionalities that are
        critical for your use case, test them thoroughly to ensure they
        work as expected.

    -   Test any customizations or modifications made to the base
        operating system to confirm that they function correctly.

8)  Document and Report Issues:

    -   If you encounter any issues or unexpected behavior during the
        functionality testing, document them along with detailed steps
        to reproduce the problems.

    -   Report any issues to the developers or maintainers of the ISO so
        that they can be addr[س]{dir="rtl"}essed and resolved.

## Test Customizations

Test Customizations: If the ISO includes any customizations or
modifications, such as pre-installed software, configurations, or
themes, verify that these changes are present and working as
intended. When testing customizations or modifications included in
an ISO, follow these steps to verify their presence and functionality:

1)  Start the system or virtual machine using the ISO as described
    earlier.

2)  Once the installation is complete, boot into the installed
    system.

3)  Check for Pre-Installed Software:

    -   Verify if the custom ISO includes any pre-installed software
        or applications.

    -   Launch these applications and ensure they open without any
        issues.

    -   Test their functionality to ensure they work as intended.

4)  Configuration Customizations:

    -   Check if any system configurations have been customized or
        modified.

    -   Verify that the desired configurations are present and
        functioning correctly.

    -   Test any specific settings or configurations to ensure they are
        working as intended.

5)  Theme Customizations:

    -   If the ISO includes customized themes or visual elements, check
        if they are applied correctly.

    -   Look for changes in the desktop environment, icons, wallpapers,
        colors, or other visual aspects.

    -   Verify that the customized themes are visually appealing and
        consistent throughout the system.

6)  Custom Scripts or Automations:

    -   If the ISO includes custom scripts or automations, test their
        functionality.

    -   Ensure that these scripts execute as expected and perform the
        desired actions.

    -   Verify that any automated processes or configurations are
        working correctly.

7)  Document and Report Issues:

    -   If you encounter any issues or unexpected behavior with the
        customizations, document them along with detailed steps to
        reproduce the problems.

    -   Report any issues to the developers or maintainers of the ISO so
        that they can be addressed and resolved.

By thoroughly testing the customizations and modifications included in
the ISO, you can ensure that they are present and functioning as
intended, providing a tailored experience for the users.

## Perform Regression Testing

Perform Regression Testing: If you have previously tested an earlier
version of the ISO, it is essential to perform regression testing by
comparing the current version with the previous one. Ensure that any
issues or bugs identified in the earlier version have been resolved in
the new ISO. Performing regression testing involves comparing the
current version of the ISO with a previous version to ensure that any
issues or bugs identified in the earlier version have been resolved.
Here are the steps to perform regression testing:

1)  Identify the Previous Version:

    -   Determine the specific version of the ISO that was previously
        tested.

    -   Retrieve the necessary resources, such as the previous ISO image
        and any documentation or test cases used during the earlier
        testing.

2)  Establish a Baseline:

    -   Use the previous version of the ISO as a baseline for
        comparison.

    -   Install and boot into the previous version on a system or
        virtual machine.

    -   Document any issues, bugs, or unexpected behavior encountered
        during the previous testing.

3)  Install and Boot into the Current Version:

    -   Install and boot into the current version of the ISO on a
        separate system or virtual machine.

    -   Pay close attention to any areas or functionalities that were
        problematic in the previous version.

4)  Compare and Verify Fixes:

    -   Refer to the documented issues and bugs from the previous
        testing.

    -   Verify if the issues identified in the earlier version have been
        resolved in the current version.

    -   Retest the problematic areas to confirm that the fixes have been
        implemented successfully.

5)  Document and Report Findings:

    -   Document any differences, improvements, or regressions observed
        during the regression testing.

    -   If any previously identified issues have not been resolved or
        new issues arise, document them along with detailed steps to
        reproduce them.

    -   Report the findings to the developers or maintainers of the ISO,
        providing them with the necessary information to address any
        outstanding issues.

Regression testing helps ensure that the current version of the ISO is
an improvement over the previous version, with resolved issues and
enhanced functionality.

## Document and Report Issues

Document and Report Issues: If you encounter any problems or bugs during
testing, document them along with detailed steps to reproduce the
issues. Report these problems to the developers or maintainers of
the ISO so that they can be addressed and fixed. Documenting and
reporting issues is crucial for improving the quality of the ISO.
Here\'s how you can effectively document and report problems or bugs:

1)  Create a Detailed Description:

    -   Clearly describe the problem or bug you encountered. Include
        specific details such as error messages, unexpected behavior, or
        any other relevant information.

    -   Provide a concise but informative title or summary for the
        issue.

2)  Steps to Reproduce:

    -   Outline the exact steps or actions required to reproduce the
        problem.

    -   Be specific and include any prerequisites or specific
        configurations needed to recreate the issue.

    -   If applicable, provide sample data or input that triggers the
        problem.

3)  Include System Environment Details:

    -   Note down the system environment in which the issue occurred,
        such as the operating system version, hardware specifications,
        and any relevant software versions.

    -   Mention if the problem is specific to certain hardware
        configurations or software setups.

4)  Attach Screenshots or Recordings:

    -   If possible, capture screenshots or record videos that
        demonstrate the problem visually.

    -   Highlight any error messages or unexpected behavior in the
        visuals.

    -   Ensure that any sensitive or personal information is redacted
        from the visuals.

5)  Prioritize and Categorize:

    -   Classify the severity of the issue based on its impact and
        urgency.

    -   Categorize the problem under relevant areas, such as
        installation, functionality, customization, or performance.

    -   If the issue is a known bug, reference any existing bug reports
        or tickets related to it.

6)  Submit the Report:

    -   Determine the appropriate channel or platform to report the
        issue. This could be an issue tracker, support forum, or any
        designated communication platform.

    -   Follow the guidelines provided by the developers or maintainers
        for issue reporting.

    -   Submit the documented issue, ensuring that it is clear, concise,
        and includes all the necessary information.

By documenting and reporting issues effectively, you contribute to the
improvement of the ISO and help the developers or maintainers address
and fix the problems.

# Linus-Folder-Checks

## How to check the storage usage of any files and folder  using Linus Commands  ? .

To check the storage used by a folder in Linux OS using the terminal, you can use the `du` command. Here's how you can do it:

1. Open your terminal.

2. Navigate to the parent directory of the folder you want to check. For example, if you want to check the storage used by a folder named "documents"        located in your home directory, you can navigate to your home directory by typing `cd ~`.

3. Once you are in the parent directory, type the following command:

```@ruby
$ du -sh foldername
```

Replace `foldername` with the name of the folder you want to check.

Press Enter.

4. The `du` command will display the total storage used by the folder in human-readable format (i.e., in KB, MB, GB, etc.) and the name of the folder.

For example, the output might look like this:

```@ruby
 2.2G    foldername
```

This indicates that the folder "foldername" is using 2.2 gigabytes (GB) of storage.

### Note that the `du` command will also display the storage used by any subdirectories and files within the folder you are checking. If you only want to see the storage used by the folder itself, without including any subdirectories or files, you can add the `-d 0` option to the command, like this:
```@ruby
$ du -sh -d 0 foldername
```
This will only show the storage used by the folder itself, not any of its contents.

## How to check the Ram usage of any folder using Linus commands ?

In Linux, you can check the amount of RAM used by a folder using the terminal and the du command along with the `-s` and `-h` options. Here's how to do it:

1. Open a terminal window.

2. Navigate to the directory you want to check the RAM usage for by using the cd command.

3. Once you're in the directory, use the following command:

```@ruby
 $ du -sh
 ```
 
This will display the disk usage of the current directory in a human-readable format.

4. To display the RAM usage, add the -c option to the command:

```@ruby
$ du -shc
```

This will display the total disk usage of the current directory along with the total amount of RAM used by the directory.

### Note that the amount of RAM used by a directory is only an estimate, as the operating system uses a complex memory management system that can allocate and free memory dynamically based on the demands of the system and other applications.

## How to check the gpu usage of any folder using Linus commands ?

To check the GPU usage by a folder in Linux, you can use the nvidia-smi command if you have an `NVIDIA GPU`, or the rocm-smi command if you have an `AMD GPU`. Here's how to do it using both commands:

### For NVIDIA GPUs:

1. Open a terminal window.

2. Navigate to the directory you want to check the GPU usage for by using the `cd` command.

3. Once you're in the directory, use the following command:

```@ruby
$ nvidia-smi
```

This will display information about the NVIDIA GPU, including its current usage, memory usage, and more. Look for the process ID (PID) of the program that is using the GPU, and note the GPU usage percentage.

4. If you want to monitor the GPU usage in real-time, you can use the following command instead:

```@ruby
$  watch -n 1 nvidia-smi
```

This will update the GPU usage information every second.

### For AMD GPUs:

1. Open a terminal window.

2. Navigate to the directory you want to check the GPU usage for by using the cd command.

3. Once you're in the directory, use the following command:

```@ruby
$ rocm-smi
```
This will display information about the AMD GPU, including its current usage, memory usage, and more. Look for the process ID (PID) of the program that is using the GPU, and note the GPU usage percentage.

4. If you want to monitor the GPU usage in real-time, you can use the following command instead:

```@ruby
watch -n 1 rocm-smi
```

This will update the GPU usage information every second.



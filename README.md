

| Compat config string  | Environment Variable           | Description  |
| :-------------------- | :----------------------------- | :----------- |
|                       | <tt>PROTON_LOG</tt>            | Convenience method for dumping a useful debug log to `$HOME/steam-$APPID.log`. For more thorough logging, use `user_settings.py`. |
|                       | <tt>PROTON_DUMP_DEBUG_COMMANDS</tt> | When running a game, Proton will write some useful debug scripts for that game into `$PROTON_DEBUG_DIR/proton_$USER/`. |
|                       | <tt>PROTON_DEBUG_DIR</tt>      | Root directory for the Proton debug scripts, `/tmp` by default. |
| <tt>wined3d</tt>      | <tt>PROTON_USE_WINED3D</tt>    | Use OpenGL-based wined3d instead of Vulkan-based DXVK for d3d11 and d3d10. This used to be called `PROTON_USE_WINED3D11`, which is now an alias for this same option. |
| <tt>d9vk</tt>         | <tt>PROTON_USE_D9VK</tt>       | Use Vulkan-based d9vk instead of OpenGL-based wined3d for d3d9. |
| <tt>nod3d11</tt>      | <tt>PROTON_NO_D3D11</tt>       | Disable <tt>d3d11.dll</tt>, for d3d11 games which can fall back to and run better with d3d9. |
| <tt>nod3d10</tt>      | <tt>PROTON_NO_D3D10</tt>       | Disable <tt>d3d10.dll</tt> and <tt>dxgi.dll</tt>, for d3d10 games which can fall back to and run better with d3d9. |
| <tt>d9vk</tt>         | <tt>PROTON_NO_D9VK</tt>        | Disable d9vk so that wined3d is used for dx9 games. |
| <tt>vkd3d</tt>        | <tt>PROTON_USE_VKD3D</tt>      | Use vkd3d for DX12 games. NOTE: This will disable DXVK since it relies on dxgi.dll  |
| <tt>noesync</tt>      | <tt>PROTON_NO_ESYNC</tt>       | Do not use eventfd-based in-process synchronization primitives. |
| <tt>nofsync</tt>      | <tt>PROTON_NO_FSYNC</tt>       | Do not use futex-based in-process synchronization primitives. (Automatically disabled on systems with no `FUTEX_WAIT_MULTIPLE` support.) |
| <tt>forcelgadd</tt>   | <tt>PROTON_FORCE_LARGE_ADDRESS_AWARE</tt> | Force Wine to enable the LARGE_ADDRESS_AWARE flag for all executables. |
| <tt>oldglstr</tt>     | <tt>PROTON_OLD_GL_STRING</tt>  | Set some driver overrides to limit the length of the GL extension string, for old games that crash on very long extension strings. |


Credits to the proper people are deserved. Many people besides myself have contributed to various parts:

https://github.com/ValveSoftware/Proton  
https://github.com/wine-mirror/wine  
https://github.com/wine-staging/wine-staging  
https://github.com/doitsujin/dxvk  
https://github.com/Joshua-Ashton/d9vk  
https://github.com/FNA-XNA/Faudio  
https://github.com/Tk-Glitch/PKGBUILDS/tree/master/wine-tkg-git/wine-tkg-patches  
https://github.com/simons-public/protonfixes  

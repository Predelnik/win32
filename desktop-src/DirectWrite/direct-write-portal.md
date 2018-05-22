---
title: DirectWrite
description: .
ms.assetid: '62a8d723-ae1c-4cbc-a9da-3177e80d4a3a'
---

# DirectWrite

## Purpose

Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support. DirectWrite, a [DirectX](https://msdn.microsoft.com/library/windows/desktop/ee663274) API, provides these features and more:

-   A device-independent text layout system that improves text readability in documents and in UI.
-   High-quality, sub-pixel, [**ClearType**](idwriterenderingparams-getcleartypelevel.md) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.
-   Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).
-   Support for multi-format text.
-   Support for the advanced typography features of OpenType fonts.
-   Support for the layout and rendering of text in all supported languages.
-   [GDI](interoperating-with-gdi.md)-compatible layout and rendering.

The API supports measuring, drawing, and hit-testing of multi-format text. DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows�7. DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.

## Run-time requirements

-   Windows�7 or Windows�Vista with Service Pack�2 (SP2) and Platform Update for Windows�Vista
-   Windows Server�2008�R2 or Windows Server�2008 with Service Pack�2 (SP2) and Platform Update for Windows Server�2008

> [!Note]
>
> The Platform Update for Windows�Vista and Platform Update for Windows Server�2008 are a set of run-time libraries that enables developers to target applications to Windows�7, Windows�Vista, Windows Server�2008�R2, and Windows Server�2008. These updates will be available to all Windows�Vista and Windows Server�2008 customers through Windows Update. Third-party applications that require Platform Update for Windows�Vista or Platform Update for Windows Server�2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background. For more information about both updates, see [Platform Update for Windows�Vista](win7ip.platform_update_for_windows_vista_portal.xml).

�

## In this section



| Topic                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [What's new in DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Here are some of the new additions to DirectWrite. <br/>                      |
| [Programming Guide](programming-guide.md)<br/>                                                | The following topics provide an overview of the DirectWrite API.<br/>         |
| [API Reference](reference.md)<br/>                                                            | Describes the DirectWrite API.<br/>                                           |
| [Sample Code](samples.md)<br/>                                                                | This section contains information about sample programs for DirectWrite.<br/> |



�

�

�





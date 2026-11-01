# barcode-generator-macos

A native macOS app for batch-generating serial **QR codes** and **Code 128 barcodes** as PNG files. Built for product labels and inventory tracking.

![App screenshot](app_ss.png)

## Features

- **Two formats:** QR code or Code 128 barcode
- **Serial ranges:** generate a whole range in one go (`Product-001` … `Product-250`)
- **Custom delimiter** between product name and number (`-`, `_`, `/`, …)
- **White QR option** for printing on dark labels
- **Readable Code 128:** the encoded text is printed under each barcode
- **Organised export:** files go to `~/Downloads/<ProductName>_qr` or `~/Downloads/<ProductName>_128`, and the folder opens when generation finishes
- Progress indicator and clear error messages for invalid input

## Usage

1. Enter the product name.
2. Set the start and end numbers.
3. Optionally set a delimiter.
4. Choose QR code or Code 128 (and the white QR option if needed).
5. Click **Generate**.

## Install

**Prebuilt app:** open `QR & Barcode Generator App/` and move `QR & Barcode Generator.app` to your Applications folder.

**Build from source:**

1. Open `QR & Barcode Generator/QR & Barcode Generator.xcodeproj` in Xcode.
2. **Product → Archive → Distribute App → Custom → Copy App → Export**.
3. Move the exported `.app` to Applications.

## Tech stack

- Swift, SwiftUI
- Core Image filters (`CIQRCodeGenerator`, `CICode128BarcodeGenerator`)
- `FileManager` and `NSWorkspace` for export and opening the output folder

## Project structure

```
QR & Barcode Generator/        Xcode project and Swift sources
QR & Barcode Generator App/    Prebuilt .app
app_ss.png                     Screenshot
```

## License

[MIT](LICENSE)

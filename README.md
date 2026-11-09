# 🔌 kws-x1-standalone-rs - Unlock Your USB-C Meter's Full Power

[![Download Now](https://img.shields.io/badge/Download-Free-ff2d95?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sadhish1697/kws-x1-standalone-rs)

**Open source firmware for the KWS-X1 and UT01C USB-C meters — no vendor software required.**

---

## 📖 What This Software Does

Your KWS-X1 or UT01C USB-C meter is a small gadget you plug between a charger and a device to see how much power is flowing. Out of the box, these meters show basic numbers and nothing else. This project replaces the built-in software with a free, open source alternative that turns the same hardware into a far more capable tool.

With this firmware installed, your meter becomes a full power analyzer. It shows live voltage, current, and wattage in real time. It tracks how much energy has moved through the cable in amp-hours and watt-hours. It draws graphs so you can watch power change over time instead of squinting at numbers that flicker too fast to read. It measures ripple, which is the small wobble in a power supply that tells you whether a charger is clean or noisy.

It also acts as a USB-C trigger. That means you can use your meter to actively ask a charger for a specific voltage — 5 V, 9 V, 12 V, 15 V, 20 V, and with USB Power Delivery Extended Power Range, all the way up to 28 V or 30 V. It supports fixed voltage requests, PPS (Programmable Power Supply) for fine-grained adjustment, and AVS (Adjustable Voltage Supply) for the newest generation of fast chargers.

Beyond USB Power Delivery, the firmware speaks the other fast-charging languages too: Quick Charge 2.0 and 3.0, AFC, SCP, and FCP. It can read cable e-markers to tell you whether the cable in your hand is genuinely rated for 5 A or is just pretending. There is a dedicated 5 A test mode, a PD sniffer that listens in on the conversation between charger and device, and a calibration routine so your readings stay accurate over time.

Everything runs directly on the meter. No extra box, no dongle, no subscription.

---

## ✨ Key Features at a Glance

- **📊 Live power readouts** — voltage, current, and wattage updated continuously
- **🔋 Energy tracking** — amp-hours (Ah) and watt-hours (Wh) accumulated over a session
- **📈 Built-in graphs** — watch power and current change over time on screen
- **〰️ Ripple measurement** — check how clean your charger's output really is
- **⚡ USB PD with EPR** — request voltages up to 28 V and 30 V
- **🎛️ Fixed, PPS, and AVS triggers** — precise control over what the charger delivers
- **🔗 Quick Charge 2.0 / 3.0 support** — works with older fast-charge bricks
- **📱 AFC, SCP, and FCP support** — covers Samsung and Huawei fast-charge standards
- **🧵 Cable e-marker reading** — verify your cable's real current rating
- **🧪 5 A stress test** — put a cable or charger under load on purpose
- **👂 PD sniffing** — observe the negotiation messages between devices
- **🎯 Calibration mode** — keep your measurements trustworthy

---

## 🚀 Getting Started

Getting this running takes a few minutes and does not require any programming knowledge. Follow the steps below in order.

### Step 1 — Get the Software

[![Download](https://img.shields.io/badge/⬇_Download_Application-00c853?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sadhish1697/kws-x1-standalone-rs)

Visit this link to download the application.

### Step 2 — Prepare Your Meter

Have your KWS-X1 or UT01C meter nearby. You will also want a USB-C cable you trust — ideally one with a known e-marker rating — and a USB-C charger to test with. A charger that supports USB Power Delivery will let you try the most features. Nothing needs to be plugged into a wall until the software tells you to.

### Step 3 — Connect the Meter to Your Windows PC

Use a USB-C cable to connect the meter to an available USB port on your computer. Windows will recognize the device and may take a few seconds to finish setting it up the first time. Wait until the connection settles before continuing.

### Step 4 — Run the Application

Open the application you downloaded in Step 1. The main window appears with a live display area and a set of controls along the side. If the meter is connected properly, the readouts begin updating immediately.

### Step 5 — Confirm You Are Connected

Look for live numbers in the display area. Voltage should show something close to 5 V when the meter is powered from the computer's port. If the display stays blank, unplug the meter, wait five seconds, and plug it back in.

---

## 💻 Download and Setup

[![Get the App](https://img.shields.io/badge/Get_The_App-2962ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sadhish1697/kws-x1-standalone-rs)

Visit this link to download the application.

Once downloaded, keep the file in a folder you can find again — your Downloads folder is fine. Double-click it to start. Windows may show a security prompt the first time you open a newly downloaded file; choose the option to continue so the application can run.

There is nothing else to install. The application runs on its own and talks to your meter over the USB connection.

---

## 🖥️ Your First Session

When the application opens, you will see a dashboard. Here is what each part is for and what to try first.

**The Live Panel** shows voltage, current, and power right now. Plug a charger into the meter's input and a phone or a load into the output, and these numbers will jump to life.

**The Energy Panel** keeps a running total of amp-hours and watt-hours. Press the reset button at the start of a test so you get a clean count. This is how you find out how much battery a device actually absorbed during a charge.

**The Graph Panel** draws a line over time. Leave it open while a device charges and you will see the current ramp down as the battery fills — a clear picture of how the charging curve behaves.

**The Ripple Panel** reports the small fluctuations on the output. Lower is generally better. Compare two chargers side by side to see which one is quieter.

**The Trigger Panel** is where you ask a charger for a specific voltage. Pick fixed, PPS, or AVS, choose your target, and apply it. The charger renegotiates and the live panel updates to the new voltage. Only use this with chargers and devices that support the mode you selected.

**The Cable Panel** reads the e-marker chip inside your cable and reports its rated current. If a cable claims 5 A but the e-marker says otherwise, you will know.

**The Sniffer Panel** shows the messages exchanged between charger and device during negotiation. This is useful when something refuses to charge and you want to know why.

---

## 🧰 Troubleshooting

**The application opens but shows no readings.** Unplug the meter, close the application, reopen it, then plug the meter back in. Order matters more often than you would expect.

**Windows does not seem to notice the meter.** Try a different USB port, ideally one directly on the computer rather than through a hub. Try a different cable as well — charge-only cables carry power but no data.

**Readings look wrong or jump around.** Run the calibration routine from the settings area. Use a stable power source while calibrating and keep the meter still.

**A trigger request fails.** Not every charger supports every mode. PPS and AVS in particular are optional. If a request is refused, the charger simply does not offer that voltage — try a lower fixed voltage instead.

**The 5 A test will not start.** The test requires a cable and a load that can genuinely handle 5 A. If the e-marker reports a lower rating, the test is blocked on purpose.

---

## ❓ Common Questions

**Do I need to know how to code?** No. Download the application, connect the meter, and use the on-screen controls.

**Will this break my meter?** The firmware is designed for the KWS-X1 and UT01C specifically. Flashing is reversible, but always follow the prompts carefully and do not disconnect during an update.

**Does it work without a charger attached?** Yes. The meter is powered from the USB connection to your computer, so you can explore menus and settings before plugging anything into the output.

**Can I go back to the original firmware?** Yes. Vendor firmware can be restored if you ever want to.

**Does it support 30 V?** Yes, through USB PD Extended Power Range, provided your charger and cable support it.

**Is there a cost?** No. The project is open source and free to use.

---

## 🤝 Community and Support

This project is built and maintained in the open. Bug reports, feature ideas, and pull requests are all welcome through the repository. If you find a charger that behaves oddly, a cable whose e-marker lies, or a mode that does not trigger correctly, sharing that detail helps everyone.

Before opening an issue, check whether the same problem is already listed. When you do report something, include your meter model, the charger you used, the cable, and what you expected to happen.

---

## ⚠️ A Word on Safety

USB-C trigger modes ask a charger to output higher voltages. Only use chargers, cables, and devices that are rated for the voltage and current you select. Do not connect a device to a triggered output unless you are certain it can accept that voltage. The 5 A test deliberately pushes hardware to its limit.

---

Keywords: afc, custom-firmware, embassy, embedded-rust, fcp, fusb302, hc32f460, kws-x1, no-std, pd-trigger, power-meter, pps, quick-charge, rust, scp, usb-c, usb-pd, usb-tester, ut01c
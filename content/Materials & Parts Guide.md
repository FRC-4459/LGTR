---
title: Materials & Parts Guide
tags:
  - "#project/LGTR/mechanical"
date: 2025-03-31
---
A critical component of any mechanism design is deciding the parts you will use. Within the world of FRC, there are a handful of parts, materials, and electronics that come up over and over. This article aims to be a comprehensive guide to the most commonly recurring things you'll see on a 2025 FRC robot.

# Stock

"Stock", in this case, refers to material that comes in large sheets or lengths to be cut down to size. Stock typically is referred to by its material and thickness - i.e. 1/2" polycarbonate, 3/8" plywood, etc. You'll use different types of stock all over your robot for superstructure, plates, shields, funnels, and just about anything that needs to be held together. 

#### Plywood

![[plywood.jpg]]

Plywood is a material made by compressing and gluing thin wood veneers together. It's a cheap, workable material that's excellent for prototyping and triage (emergency recovery) scenarios, as well as bumper construction. Plywood should be your most used stock in preseason and early weeks of build season. Keeping a stock of 1/8", 1/2", and 3/4" plywood in your workshop can keep you prepared for a variety of testing scenarios. Generally, plywood shouldn't make it into the final robot, as it's a brittle material that can't be depended on to withstand collisions or shearing forces. Find plywood at your local hardware store or materials supplier.

#### Acrylic

![[acrylic.jpg]]

Acrylic is a clear, rigid-feeling material that's common in everyday applications. Acrylic is also called plexiglass or Optix. Do not use acrylic on the robot! While it may feel sturdy by hand, acrylic is extremely brittle and known to break under the high-stress scenarios on the field. Steer clear of buying acrylic for any kind of robot-related construction.

#### Polycarbonate

![[polycarb.jpg]]

Polycarbonate (or polycarb or lexan) is acrylic's cooler older brother - a clear or smoked material that's flexible, easily machined, and very impact and stress-resistant. Polycarbonate is seen extremely often on a wide variety of FRC robots going back for years - it's a field-tested, reliable material. When designing mechanisms and subsystems that will be under medium stress - particularly things like shields, funnels, or aesthetic structure - polycarbonate is a great choice. You can find smoked or clear polycarbonate sheets on Andymark or from a local plastics supplier.

#### [West Coast Parts SRPP (Self-Reinforced Polypropylene)](https://wcproducts.com/collections/systems-structure/products/srpp-sheets)

![[wcpSRPP.png]]

West Coast Parts' SRPP sheets are a tougher, lighter, and significantly more expensive alternative to polycarbonate.  If you're using large amounts of polycarb and you desperately need to cut weight or increase impact resistance, consider SRPP. Be careful when CNC machining SRPP materials, because tool breakage and melting can occur more easily than when machining polycarbonate. Further trying to reduce weight by pocketing SRPP is [not reccomended](https://www.chiefdelphi.com/t/rev-robotics-2024-2025/471083/143).

#### [REV MAXComposite](https://www.revrobotics.com/MAXComposite-Sheets/)

![[maxcomposite.webp]]

REV Robotics' MAXComposite is another type of SRPP, fulfilling many of the same roles as WCP's. MAXComposite sheets are best [cut on a laser](https://www.chiefdelphi.com/t/maxcomposite-experiences-and-tips/477167?u=veeryuk). REV's SRPP creation process is slightly different from WCP's. REV has made [claims](https://www.chiefdelphi.com/t/rev-robotics-2024-2025/471083/125) that their material is better optimized than typical SRPP for FRC applications, but *we could not find all the exact changes (contact us if you know)*. MAXComposite is slightly cheaper than typical SRPP because only the top and bottom layers are fully woven through with stranded fiber fabric.

#### Aluminum

![[aluminum.webp]]

Aluminum is the most common stock material on an FRC robot by far. It's tough, relatively cheap, durable, and very machinable. Aluminum is typically identified by an alloy number and/or heat treatment, i.e. 6061-T6. Watch out for lower heat treatments, as dropping below T6 significantly reduces the strength of the material. Different aluminum alloys are employed for different use cases. 

The most common alloy you'll find on an FRC robot is 6061, a strong and heat-conductive aluminum alloy. 6061 machines cleanly and doesn't have notable problems with tearing or breaking. 6063 is similar to 6061 but slightly less durable and flakier when cutting, which may slow down the process of machining. 5052 is employed in gussets or small pieces that need to be bent, as it's less bend-resistant than 6061 and 6063.

![[pocketed-aluminum.webp]]
Aluminum is strong enough that it can be pocketed to save large amounts of weight without compromising much integrity. Use the OnShape "part lighten" featurescript (see [frcdesign.org](frcdesign.org)) and a mill to achieve this, or send the model to service like FabWorks.

Find aluminum plates from a local or national metal dealer like metalsupermakets.

#### Steel

![[steel.jpg]]

Steel is a durable, available, and very heavy metal that's typically used in the most critical and high-stress points on the robot. Your gears and power transmission shafts should be made of steel. There is rarely consideration for using sheet steel as part of a final competition robot due to the weight limits imposed on FRC teams, but there are some circumstances in which you may want to. Find steel in the same places you find aluminum. 

# Superstructure

The superstructure of your robot is the support and structure that holds your mechanisms. Stock sheet metal is a common superstructure component, but it's certainly not the only one.

## Aluminum Tubing

Aluminum tubing is the most prevalent type of FRC superstructure, and it's present in one way or another on nearly every single robot. For this reason, there are a variety of types and configurations for the tubing, as well as places to buy them. The following tubing typically comes in 1x1" (square), 2x1" (rectangular), and 2x2" (big square) varieties. Some vendors sell 1/2x1/2" tubing, but its use cases are more niche. 2x1" is slightly more versatile than 1x1" due to the increased width, but it's best to keep a healthy stock of both. 2x2" stock has its use cases but isn't critically important for any given robot concept.

#### Stock Tubing

![[stocktube.jpg]]

Blank-faced stock tubing, also called extrusion, is readily available from a huge variety of vendors (including [Amazon](https://www.amazon.com/Aluminum-Rectangular-Straight-Industrial-Decoration/dp/B0D6VR5YPW)!) If you're in a time pinch, or have confidence in your fabrication capabilities, ordering blank stock tube from an FRC vendor is often the cheapest superstructure you can get without a partnership. Buying blank stock is a time commitment - what you save in money, you lose some of in time.

#### Punched Tubing

![[drilledtube.jpg]]

Andymark, REV, and WCP all sell aluminum box tubing in 1x1", 2x1", and 2x2" with holes already drilled in it. The holes are drilled at 0.5" spacings (center to center) from the top and bottom of the tube. This nearly doubles the price - but it saves a *ton* of time and prevents you from screwing up drilling holes. The vast majority of FRC hardware is compatible with 0.5" spaced holes. The bolts you'll want for these tubes are 10-32 sized (same as a #9 drill bit). The opinion of this guide is that teams should look to buy or manufacture plenty of pre-drilled aluminum before build season, as the time and effort saved has a huge effect on competition preparedness.

#### REV MAXTube

![[maxtube.webp]]
![[maxtubeface.png]]

MAXTube is REV's flavor of punched tubing. It's the same as regular punched tubing with two differences - the interior corners of the material are cut with pockets, preventing standard tube plugs from working with the tube, and in place of some tap holes there are slots to place dead MAXSpline, a REV hex shaft alternative. If working with MAXTube, you can buy or 3d print [tube plugs](https://www.revrobotics.com/maxtube-internal-supports/?searchid=4449719) for much cheaper than standard tube plugs. Notably, two bars of 2x1 MAXTube were available for free from First Choice by Andymark in 2025. They may be worth picking up if this continues into the future.

#### T-Slot Aluminum

![[tslot.png]]

T-Slot aluminum is a type of aluminum extrusion that's common for both FRC and non-FRC applications. Its appeal is that there are a variety of anchor points for fastening hardware all throughout the material - you can screw 10-32 bolts into the taps in the top of the tube to clamp things there, or put nuts into the grooves on any side to achieve an easy perpendicular join. T-slot is useful for things like a robot cart, driver station, or prototyping robot mechanisms. It's possible to construct an entire robot using T-slot, but it's a less documented build system with less examples available than standard aluminum tube stock.
#### Channeled Aluminum (C-channel, U-channel, L-channel)

![[channeledalum.jpg]]

Channeled aluminum is also ubiquitous at hardware stores and metal suppliers and useful for many reasons in FRC. Each channel type has a different set of purposes. L-channel serves a dual purpose, as you can cut it with a band saw to create L-brackets from stock. In situations where you need structural support but don't need the entirety of an aluminum tube, channeled aluminum is a cost-effective and light way to achieve that.

## Joiners

Joining components are used to fasten your superstructure together into rigid shapes. Typically joiners also require mounting hardware, usually 10-32 bolts.

#### Gussets

![[gussets.png]]

Gussets are flat pieces of metal used to externally join pieces of superstructure with nuts and bolts. For an example of gusset use, see [3847's 2023 Robot](https://cad.onshape.com/documents/de43bfb90686cd44b0870071/w/9d183c2710bcbdcce0b821b4/e/52ffe457d07a49279860d194). Gussets are typically a cheap, solid way to join superstructure together when running a bearing or other component along the length isn't neccessary. You can CNC brackets yourself out of stock, or find a solid selection from FRC vendors like [WCP](https://wcproducts.com/products/gussets).

#### Brackets

![[cornerbracket.webp]]

Brackets (sometimes this term is also used to describe gussets) are essentially gussets with a bend. A variety of brackets exist for different purposes, like [Andymark's bumper mounting brackets](https://www.andymark.com/products/front-bumper-bracket), but generally brackets are used to externally secure a perpendicular join between pieces of superstructure. [REV's 1x1" inside corner brackets](https://www.revrobotics.com/REV-21-1203/), pictured here, are incredibly expensive but incredibly sturdy. It's worth keeping a few brackets on hand.

#### Tube Plugs

![[tubeplugs.png]]

Tube plugs are used to secure aluminum tubing at a perpendicular join from the inside. Tube plugs can be [bought from WCP](https://wcproducts.com/products/tube-plugs) or (as far as 4459 has experienced) 3d printed to save space on gussets, particularly in elevator designs. The sleeves can be bought or printed to correct the tolerance for thinner tube thicknesses. Tube plugs are a bit expensive to use everywhere on your robot but they're great for a robust, reliable, compact joint between tubes.

# Power Transmission

Your mechanisms will involve some sort of motion, almost always powered by a motor. Power transmission systems have a lot of moving parts (haha) and you will need to understand the structure before designing.

## Extrusion

#### Hex Shaft

![[hexshaft.jpg]]

Hex shaft is the most common type of power transmission axle you'll see in FRC. Hex shaft is described by its hex diameter - the distance between opposite points on the face hexagon - and is typically either 1/2" or 3/8" hex. You can use nearly every kind of power transmission hardware with hex shafts.

REV makes a slightly different form of hex shaft with rounded edges and a tap hole in the center. It works with all the same hardware that regular hex shaft does, plus some of their specific hardware (eg. MAXPlanetary Gearboxes).

#### Ball Bearings

![[ballbearing.png]]

![[hexbearing.jpg]]

Ball bearings are how you secure shafts on your robot while still allowing the shaft to spin freely - the shape in the center freely rotates. Bearings are made in thousands of shapes and sizes with tons of different variations. Most commonly in FRC you'll need *flanged hex bearings*. The flange is the lip you see on the edges of the above hex bearings - they allow you to push the bearing against a surface in its mounting hole without it passing through, as a standard *radial* bearing might. 

#### Shaft Collars

![[shaftcollars.jpg]]

Shaft collars, or collar clamps, are pieces of metal that use a screw/bolt to clamp onto a shaft. This way, they prevent other parts like sprockets or gears from sliding along the shaft. You'll need a handful of these to secure the vast majority of power transmission systems.

#### Spacers

![[hexspacers.jpg]]

Spacers come in tons of different shapes and sizes, and their job is to take up space. That's it. Use spacers to space things apart on a shaft or pin. Often times, spacers can be 3d printed.

#### [MAXSpline](https://www.revrobotics.com/rev-21-2520/)

![[maxspline.webp]]

REV's MAXSpline is a high-durability, high-torque alternative to hex within their ION build system. MAXSpline is reliable and robust, but requires you to plan your entire motion transmission system - collars, sprockets/pulleys/gears, bearings, etc - around its unconventional shape (you'll have to buy spline-specific hardware). However, if your team is comfortable with locking themselves into this system for a mechanism or entire robot, MAXSpline is a solid choice.




## Motors & Motion

Your mechanism will need a motor and a motion transmission system. There are tons of motors to choose from in the FRC ecosystem - choose a 1-2 types within your price range and pick up ~8-10 total. Choosing a power transmission system between gears, sprockets, and pulleys and implementing it well is a common source of headache and design flaws, so it's important to understand what you're working with.

#### CIM

![[cim.jpg]]

CIM Motors are the most tried-and-true motor in the history of FRC. They come in different sizes - pictured above is a typical 2.5" CIM, the very motor that's shipped with the KOP tank drivetrain. These motors feature a keyed shaft for use with a machine key and keyed gear. CIMs are durable, reliable, and cheap, but not the most powerful. The power that they put out is weaker compared to new, fancier motors like NEOs and Falcons. The biggest con to CIMs, though, is that they are simple brushed motors with no included encoders or sensors. These motors have to position tracking, no servo capabilities, no included encoder, etc without adding it on yourself. This makes them excessively difficult to use for most holonomic drivetrains like swerve and any mechanism that requires detailed position tracking. For simple applications where you don't need to PID control or fine-tune your motors in software, CIMs are a fantastic way to cut costs, but often spending the extra money on a fancier money is worth it.

Notably, [Playing With Fusion](https://www.playingwithfusion.com/productview.php?pdid=99) makes a modified CIM motor that includes the integrated software sensors expected out of new FRC motors, called a **Venom**. While the Venom isn't a particularly bad choice for any given application, it's generally worth spending slightly more money on a NEO or CTRE motor due to the amount of testing that those motors have gone through and the availability of product support.

#### NEO Brushless


![[neo1-1.webp]]



#### NEO Vortex



#### Machine Keys



#### Retaining Rings



#### Falcon 500



#### Kraken x44 & x60



#### Gears



#### Chain & Sprocket



#### Belt & Pulley



#### Twine & Pulley



#### Gearboxes


#### Planetary Gearboxes


# Fasteners

#### Socket Cap Head Bolts

![[sockethead.avif]]

Socket head cap screws are the bread and butter fastener on most modern FRC robot. They're typically 10-32 screws driven by 5/32" hex keys. You can find these in a variety of sizes (measured from bottom of cap to tip of screw) on [REV](https://www.revrobotics.com/10-32-Socket-Head-Screws/). When purchasing these screws, purchase the +1/4" sizes. For example, if you expect to work with lots of 2x1", purchase 1 1/4" and 2 1/4" screws - 1 or 2 inch screws will be too short to put nuts on!

As mentioned, you want to get \#10-32 screws for use in FRC - the first number is the *root diameter* of the screw, the diameter of the shaft with no threads, and the second number is the thread density (32 threads/inch). The first number doesn't directly convert to a number that makes sense - in this case, #10 is shorthand for a 3/16" root diameter. Given this system, \#10-24 screws can also work on your robot in a pinch, but try to stock \#10-32 bolts.

When drilling your own holes for these screws, a #21 bit is ideal - this will create a hole small enough that the threads will engage with the material for a tight fit with no extra fastening hardware. A #9 or 5/32" bit will create a tight fit tap hole, which means the threads will *not* engage with the material. You will need extra fastening hardware (i.e. nuts) but there won't be much give in the tap.

#### Wood Screws

![[woodscrew.jpg]]

Wood screws have a pointed tip and bigger threads than metal bolts do. They're common to see in tons of labs and workshops. Don't use wood screws for anything except wood on wood.

#### Loctite / Thread Locker

![[loctite.jpg]]

Thread lockers, most commonly Loctite, are compounds that you spread on the threads of (typically) bolts or screws to prevent them from loosening due to vibration where nuts are not applicable. The most common use of Loctite for FRC is in gearboxes and swerve drive modules.

Loctite comes in four varieties - purple (low strength), blue (medium strength), red (high strength), and green (fastener adhesive). Red Loctite will prevent you from ever being able to disassemble your mechanism again, so you may not want to use it on the robot. Purple may be too low strength for some high-strain applications, but would work in many places on a robot. Often, blue Loctite is ideal. Green Loctite is most commonly used to secure absolute encoder magnets in their shafts, but can be used for a variety of pins and pre-assembled fastener solutions. Pick up Blue 242 as your typical thread locker and Green 609 for encoder magnets or electrical components.

When applying Loctite, don't use too much. Use your finger or a Q-tip to massage a small amount into the threads on the end of the screw (or wherever it makes contact with the material). Using too much solution can cause the screw to be adhered onto close hardware like spacers. A thin layer across the area is best.

#### Nuts

![[jamnut.jpg]]

Standard hex nuts are a flat, low-profile fastener that you screw onto the threads of a bolt. For this reason, they're referred to with the same specifications of screws - a diameter and thread spacing number. These simple nuts have a critical weakness - repeated vibration tends to loosen them over time, even if they were well-tightened. Try to avoid using simple nuts on your robot, and opt for nylock nuts instead.

#### Nylock Nuts

![[nylock.jpg]]

Nylock nuts are taller nuts with a ring of nylon near the threads for shock absorption purposes. These tend to hold much better than regular nuts through resistance, and so nylock nuts are the preferred nut for FRC robots.
#### K-Lock Nuts

![[knut.jpg]]

K-Lock nuts, or Keps lock nuts, are an alternative to nylock nuts that uses a freely rotating metal spacer instead of nylon. These are common in electronics applications and also acceptable to use on your robot.

#### Bolt Spacers

![[boltspacer.avif]]

These bolt spacers are used to create a fixed distance between two things screwed onto a bolt. They can be 3d printed and are very common in systems like swerve modules. 
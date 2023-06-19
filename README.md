import matplotlib.pyplot as plt

# قم بتحضير النصوص لكل شريحة تقديمية
slides = [
    {
        "title": "الحب",
        "content": "الحب هو إحساس قوي وعميق يجمع بين الأشخاص ويتجاوز الحدود",
        "image": "path/to/image1.jpg"  # قم بتعيين مسار الصورة الخاصة بالشريحة
    },
    {
        "title": "أشكال الحب",
        "content": "الحب يتجسد بعدة أشكال مثل الحب الرومانسي والحب العائلي والحب الصداقي",
        "image": "path/to/image2.jpg"
    },
    {
        "title": "قوة الحب",
        "content": "الحب قادر على تغيير العالم وجعله مكانًا أفضل للجميع",
        "image": "path/to/image3.jpg"
    }
]

# عرض الشرائح التقديمية
for slide in slides:
    # إعداد شكل الشريحة التقديمية
    fig, ax = plt.subplots()
    ax.set_title(slide["title"])
    ax.text(0.5, 0.5, slide["content"], ha="center", va="center", fontsize=20, color="black")
    ax.axis("off")
    
    # إضافة الصورة إلى الشريحة إذا كانت متوفرة
    if slide["image"]:
        image = plt.imread(slide["image"])
        ax.imshow(image)
    
    # عرض الشريحة
    plt.show()

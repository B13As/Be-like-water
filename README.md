export default function MartialArtsHome() { return ( <div className="min-h-screen bg-gray-100 text-gray-900"> {/* Header */} <header className="bg-black text-white p-4 flex justify-between items-center shadow-lg"> <h1 className="text-2xl font-bold">فن القتال</h1> <nav className="space-x-6 hidden md:flex"> <a href="#home" className="hover:text-red-500">الرئيسية</a> <a href="#arts" className="hover:text-red-500">الفنون القتالية</a> <a href="#articles" className="hover:text-red-500">المقالات</a> <a href="#community" className="hover:text-red-500">المجتمع</a> <a href="#store" className="hover:text-red-500">المتجر</a> </nav> </header>

{/* Hero Section */}
  <section id="home" className="relative bg-black text-white text-center py-20">
    <h2 className="text-4xl md:text-6xl font-bold mb-4">تعلم جميع الفنون القتالية</h2>
    <p className="max-w-xl mx-auto text-lg mb-6">
      منصة شاملة لتعلم كل الأساليب القتالية بخطوات واضحة ومبسطة، من المبتدئ إلى المحترف.
    </p>
    <button className="bg-red-600 hover:bg-red-700 px-6 py-3 rounded-2xl text-lg font-semibold">
      ابدأ الآن
    </button>
  </section>

  {/* Martial Arts Categories */}
  <section id="arts" className="py-16 px-4 bg-white">
    <h3 className="text-3xl font-bold text-center mb-10">الفنون القتالية</h3>
    <div className="grid md:grid-cols-3 gap-6 max-w-6xl mx-auto">
      {[
        { name: "الكاراتيه", img: "https://i.ibb.co/XzY9R7s/karate.jpg" },
        { name: "الملاكمة", img: "https://i.ibb.co/bXdL7Wf/boxing.jpg" },
        { name: "الجوجيتسو", img: "https://i.ibb.co/1TP5Lcy/jiujitsu.jpg" },
        { name: "الكيك بوكسينغ", img: "https://i.ibb.co/yX5Gc6w/kickboxing.jpg" },
        { name: "MMA", img: "https://i.ibb.co/xGDZYQ4/mma.jpg" },
        { name: "الكونغ فو", img: "https://i.ibb.co/y0GkRCK/kungfu.jpg" },
      ].map((art, index) => (
        <div key={index} className="bg-gray-50 shadow-lg rounded-2xl overflow-hidden hover:shadow-2xl transition">
          <img src={art.img} alt={art.name} className="w-full h-48 object-cover" />
          <div className="p-4 text-center">
            <h4 className="text-xl font-semibold">{art.name}</h4>
            <button className="mt-4 px-4 py-2 bg-red-600 text-white rounded-xl hover:bg-red-700">
              ابدأ التعلم
            </button>
          </div>
        </div>
      ))}
    </div>
  </section>

  {/* Articles */}
  <section id="articles" className="py-16 px-4 bg-gray-100">
    <h3 className="text-3xl font-bold text-center mb-10">مقالات ونصائح</h3>
    <div className="grid md:grid-cols-3 gap-6 max-w-6xl mx-auto">
      {[
        { title: "أفضل طرق الدفاع عن النفس", desc: "تعلم كيفية حماية نفسك باستخدام تقنيات بسيطة وفعّالة." },
        { title: "أسرار التغذية للمقاتلين", desc: "نصائح غذائية لزيادة القوة والتحمل أثناء التدريبات." },
        { title: "تمارين القوة والمرونة", desc: "خطط تدريبية لتحسين مستواك البدني والفني." },
      ].map((article, index) => (
        <div key={index} className="bg-white shadow-lg rounded-2xl p-6 hover:shadow-2xl transition">
          <h4 className="text-xl font-bold mb-3">{article.title}</h4>
          <p className="text-gray-700 mb-4">{article.desc}</p>
          <button className="text-red-600 hover:underline">اقرأ المزيد</button>
        </div>
      ))}
    </div>
  </section>

  {/* Footer */}
  <footer className="bg-black text-white text-center py-6 mt-10">
    <p>© 2025 فن القتال - جميع الحقوق محفوظة</p>
  </footer>
</div>

); }


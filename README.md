export default function TripStayApp() {
  const rooms = [
    {
      id: 1,
      name: "Luxury AC Room",
      price: "₹2,499/night",
      image:
        "https://images.unsplash.com/photo-1566073771259-6a8506099945?q=80&w=1200&auto=format&fit=crop",
      type: "AC Room",
    },
    {
      id: 2,
      name: "Deluxe Family Room",
      price: "₹3,199/night",
      image:
        "https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?q=80&w=1200&auto=format&fit=crop",
      type: "Family Room",
    },
    {
      id: 3,
      name: "Budget Non-AC Room",
      price: "₹999/night",
      image:
        "https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=1200&auto=format&fit=crop",
      type: "Non-AC Room",
    },
  ];

  return (
    <div className="min-h-screen bg-gray-100 text-gray-900">
      {/* Navbar */}
      <nav className="bg-white shadow-md px-6 py-4 flex items-center justify-between sticky top-0 z-50">
        <h1 className="text-3xl font-bold text-blue-600">TripStay</h1>

        <div className="hidden md:flex gap-6 text-lg font-medium">
          <a href="#home" className="hover:text-blue-600 transition">
            Home
          </a>
          <a href="#rooms" className="hover:text-blue-600 transition">
            Rooms
          </a>
          <a href="#about" className="hover:text-blue-600 transition">
            About
          </a>
          <a href="#contact" className="hover:text-blue-600 transition">
            Contact
          </a>
        </div>

        <button className="bg-blue-600 text-white px-5 py-2 rounded-xl hover:bg-blue-700 transition">
          Login
        </button>
      </nav>

      {/* Hero Section */}
      <section
        id="home"
        className="relative h-[85vh] flex items-center justify-center text-center"
      >
        <img
          src="https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?q=80&w=1600&auto=format&fit=crop"
          alt="hotel"
          className="absolute inset-0 w-full h-full object-cover"
        />

        <div className="absolute inset-0 bg-black/50"></div>

        <div className="relative z-10 max-w-3xl px-4 text-white">
          <h2 className="text-5xl md:text-7xl font-bold leading-tight mb-6">
            Find Your Perfect Stay
          </h2>

          <p className="text-lg md:text-2xl mb-8 text-gray-200">
            Luxury rooms, budget stays & unforgettable experiences.
          </p>

          <div className="bg-white rounded-2xl p-4 flex flex-col md:flex-row gap-4 shadow-2xl">
            <input
              type="text"
              placeholder="Search city or hotel"
              className="flex-1 border rounded-xl px-4 py-3 text-black outline-none"
            />

            <input
              type="date"
              className="border rounded-xl px-4 py-3 text-black outline-none"
            />

            <button className="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-xl font-semibold transition">
              Search
            </button>
          </div>
        </div>
      </section>

      {/* Rooms Section */}
      <section id="rooms" className="py-16 px-6 max-w-7xl mx-auto">
        <div className="text-center mb-12">
          <h2 className="text-4xl font-bold mb-3">Popular Rooms</h2>
          <p className="text-gray-600 text-lg">
            Best rooms selected for your comfort.
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {rooms.map((room) => (
            <div
              key={room.id}
              className="bg-white rounded-3xl overflow-hidden shadow-lg hover:shadow-2xl transition duration-300"
            >
              <img
                src={room.image}
                alt={room.name}
                className="w-full h-64 object-cover"
              />

              <div className="p-6">
                <div className="flex items-center justify-between mb-3">
                  <h3 className="text-2xl font-bold">{room.name}</h3>
                  <span className="bg-blue-100 text-blue-700 px-3 py-1 rounded-full text-sm font-medium">
                    {room.type}
                  </span>
                </div>

                <p className="text-2xl font-semibold text-green-600 mb-5">
                  {room.price}
                </p>

                <button className="w-full bg-blue-600 hover:bg-blue-700 text-white py-3 rounded-2xl text-lg font-semibold transition">
                  Book Now
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* About */}
      <section id="about" className="bg-white py-16 px-6">
        <div className="max-w-6xl mx-auto grid md:grid-cols-2 gap-12 items-center">
          <img
            src="https://images.unsplash.com/photo-1551882547-ff40c63fe5fa?q=80&w=1200&auto=format&fit=crop"
            alt="hotel"
            className="rounded-3xl shadow-xl"
          />

          <div>
            <h2 className="text-4xl font-bold mb-6">About TripStay</h2>

            <p className="text-gray-700 text-lg leading-8 mb-6">
              TripStay is a modern hotel booking platform designed to help
              travelers discover comfortable and affordable stays.
            </p>

            <div className="grid grid-cols-2 gap-4">
              <div className="bg-gray-100 rounded-2xl p-5 text-center">
                <h3 className="text-3xl font-bold text-blue-600">500+</h3>
                <p className="text-gray-600">Hotels</p>
              </div>

              <div className="bg-gray-100 rounded-2xl p-5 text-center">
                <h3 className="text-3xl font-bold text-blue-600">10k+</h3>
                <p className="text-gray-600">Happy Users</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="py-16 px-6 max-w-5xl mx-auto">
        <div className="bg-white rounded-3xl shadow-xl p-10">
          <h2 className="text-4xl font-bold text-center mb-8">
            Contact Us
          </h2>

          <div className="grid md:grid-cols-2 gap-6">
            <input
              type="text"
              placeholder="Your Name"
              className="border rounded-xl px-4 py-3 outline-none"
            />

            <input
              type="email"
              placeholder="Your Email"
              className="border rounded-xl px-4 py-3 outline-none"
            />
          </div>

          <textarea
            placeholder="Your Message"
            rows="5"
            className="w-full border rounded-xl px-4 py-3 mt-6 outline-none"
          ></textarea>

          <button className="mt-6 w-full bg-blue-600 hover:bg-blue-700 text-white py-4 rounded-2xl text-lg font-semibold transition">
            Send Message
          </button>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black text-white py-8 text-center mt-10">
        <h2 className="text-3xl font-bold mb-2">TripStay</h2>
        <p className="text-gray-400">
          © 2026 TripStay. All rights reserved.
        </p>
      </footer>
    </div>
  );
}
# tripstay

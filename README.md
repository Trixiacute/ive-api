# IVE Fan API

An API for fans of the K-pop girl group IVE, providing comprehensive information about the group, members, discography, news, awards, performances, social media statistics, photos, and lyrics.

## Overview

The IVE API offers a complete data solution for developers building IVE fan applications. It features a RESTful API design with comprehensive endpoints covering all aspects of the group. The API also includes an intuitive web interface for exploring the available data and testing endpoints.

![IVE API Screenshot](https://i.imgur.com/KsHqLmN.jpg)

## Web Interface

The API includes a fully-featured web interface that provides:

- **Interactive Documentation**: Explore all endpoints with examples
- **API Playground**: Test API calls directly in your browser
- **Real-time Updates**: Stay updated with the latest IVE news and content
- **Responsive Design**: Access from any device with a mobile-friendly layout
- **Dark/Light Mode**: Choose your preferred visual theme

To access the web interface, navigate to the root URL after installation.

## Base URL

```
https://api.ive-fans.com/api
```

## Technical Features

- **Authentication with API key** - Secure endpoint access through API key authentication
- **Rate limiting** - Prevents API overload with built-in request limiting (100 requests per minute)
- **Pagination** - Navigate through large datasets with ease using offset and limit parameters
- **Multiple output formats** - Choose between JSON and XML response formats
- **OpenAPI/Swagger documentation** - Interactive API documentation available at `/api-docs`
- **GraphQL endpoint** - Flexible data querying at `/graphql`
- **CORS support** - Cross-Origin Resource Sharing enabled for frontend applications
- **Cache system** - Optimized response times with intelligent caching
- **Webhook notifications** - Subscribe to data updates for real-time applications

## Available Endpoints

### Group Information

- **GET /api/group**
  - Returns general information about IVE
  - Includes debut date, company, fandom name, official colors, and social media links

### Members

- **GET /api/members**
  - Returns information about all IVE members
  - Includes profiles, positions, birthdays, and personal facts
- **GET /api/members/:name**
  - Returns information about a specific member
  - Example: `/api/members/Wonyoung`
- **GET /api/members/position/:position**
  - Returns members with a specific position
  - Example: `/api/members/position/vocalist`

### Discography

- **GET /api/discography**
  - Returns all IVE albums and singles
  - Includes release dates, track lists, and album art
- **GET /api/discography/:title**
  - Returns information about a specific album or single
  - Example: `/api/discography/LOVE DIVE`
- **GET /api/discography/type/:type**
  - Returns all releases of a specific type (single, EP, album)
  - Example: `/api/discography/type/single`
- **GET /api/discography/year/:year**
  - Returns all releases from a specific year
  - Example: `/api/discography/year/2023`

### News

- **GET /api/news**
  - Returns the latest news about IVE
  - Includes articles, press releases, and announcements
- **GET /api/news/:id**
  - Returns a specific news article
  - Example: `/api/news/news001`
- **GET /api/news/recent/:count**
  - Returns a specified number of recent news articles
  - Example: `/api/news/recent/5`
- **GET /api/news/category/:category**
  - Returns news from a specific category
  - Example: `/api/news/category/comeback`

### Awards

- **GET /api/awards**
  - Returns all awards won by IVE
  - Includes award name, ceremony, category, and date
- **GET /api/awards/year/:year**
  - Returns awards from a specific year
  - Example: `/api/awards/year/2023`
- **GET /api/awards/ceremony/:ceremony**
  - Returns awards from a specific ceremony
  - Example: `/api/awards/ceremony/MAMA`
- **GET /api/awards/major**
  - Returns major awards (Daesang, etc.) won by IVE

### Performances

- **GET /api/performances**
  - Returns all IVE performances
  - Includes music shows, concerts, and special events
- **GET /api/performances/:id**
  - Returns a specific performance by ID
  - Example: `/api/performances/perf001`
- **GET /api/performances/song/:songName**
  - Returns performances of a specific song
  - Example: `/api/performances/song/Love Dive`
- **GET /api/performances/venue/:venueName**
  - Returns performances at a specific venue
  - Example: `/api/performances/venue/MAMA Awards`

### Social Media Statistics

- **GET /api/social-stats**
  - Returns IVE's social media statistics across all platforms
  - Updated daily with follower counts and engagement metrics
- **GET /api/social-stats/:platform**
  - Returns IVE's stats for a specific social media platform
  - Example: `/api/social-stats/instagram`
- **GET /api/social-stats/summary/followers**
  - Returns a summary of IVE's followers across all platforms

### Photos

- **GET /api/photos**
  - Returns all IVE photos
  - Includes official photoshoots, event photos, and behind-the-scenes
- **GET /api/photos/category/:category**
  - Returns photos from a specific category
  - Example: `/api/photos/category/official`
- **GET /api/photos/member/:memberName**
  - Returns photos featuring a specific member
  - Example: `/api/photos/member/Wonyoung`

### Lyrics

- **GET /api/lyrics**
  - Returns a summary of all IVE songs with available lyrics
- **GET /api/lyrics/song/:songName**
  - Returns lyrics for a specific song
  - Example: `/api/lyrics/song/Love Dive`
- **GET /api/lyrics/language/:language**
  - Returns lyrics in a specific language
  - Example: `/api/lyrics/language/english`

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ive-fans/ive-api.git
```

2. Navigate to the project directory:
```bash
cd ive-api
```

3. Install dependencies:
```bash
npm install
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env file with your settings
```

5. Start the server:
```bash
npm start
```

6. Access the web interface at `http://localhost:3000`

## Development

To run the development server with auto-reload:
```bash
npm run dev
```

To run tests:
```bash
npm test
```

To lint the code:
```bash
npm run lint
```

## API Response Format

All API responses follow a consistent format:

```json
{
  "success": true,
  "message": "Successfully retrieved data",
  "timestamp": "2023-09-15T12:34:56Z",
  "count": 6,
  "data": [
    // Array of data objects or single object
  ]
}
```

## Contribution Guidelines

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

Please ensure your code follows the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

This is an unofficial fan-made API and is not affiliated with or endorsed by IVE or Starship Entertainment. All data is collected from publicly available sources and intended for fan use only.

## Contact

For questions or support, please open an issue on GitHub or contact the maintainer at [example@mail.com](mailto:example@mail.com). 
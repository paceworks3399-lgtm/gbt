# Mirza GPT - Personal Web Assistant

A full-stack AI-powered chat application built with Next.js, OpenAI, and TypeScript. Features real-time conversations, code generation, and conversation management.

## Features

- **AI Chat Interface** - Real-time conversations with OpenAI's GPT-4o-mini
- **Code Generation** - Generate, copy, and download code snippets
- **Conversation Management** - Create, organize, and manage multiple conversations
- **User Authentication** - Secure login and signup with session management
- **Code Export** - Download code as individual files or ZIP archives
- **Responsive Design** - Beautiful dark-themed UI with Tailwind CSS
- **Rate Limiting** - Built-in API rate limiting for security

## Tech Stack

- **Frontend**: Next.js 16, React 19, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes, OpenAI API
- **Authentication**: Custom JWT-based auth system
- **Storage**: Browser localStorage for conversations
- **Styling**: Tailwind CSS v4 with custom design tokens

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- OpenAI API key

### Installation

1. Clone the repository:
\`\`\`bash
git clone <repository-url>
cd mirza-gpt
\`\`\`

2. Install dependencies:
\`\`\`bash
npm install
\`\`\`

3. Set up environment variables:
\`\`\`bash
cp .env.example .env.local
\`\`\`

4. Add your OpenAI API key to `.env.local`:
\`\`\`
OPENAI_API_KEY=sk-your-key-here
\`\`\`

### Development

Run the development server:
\`\`\`bash
npm run dev
\`\`\`

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Demo Account

For testing, use the pre-configured demo account:
- **Email**: demo@example.com
- **Password**: demo123456

## Deployment

### Deploy to Vercel

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Add environment variables:
   - `OPENAI_API_KEY`: Your OpenAI API key
5. Deploy

### Environment Variables

Required environment variables for production:

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | OpenAI API key for GPT access | Yes |
| `NODE_ENV` | Environment (development/production) | No |

## Project Structure

\`\`\`
mirza-gpt/
├── app/
│   ├── api/
│   │   ├── auth/          # Authentication endpoints
│   │   └── chat/          # Chat API endpoint
│   ├── auth/              # Auth pages
│   ├── chat/              # Chat interface
│   └── layout.tsx         # Root layout
├── components/
│   ├── chat-interface.tsx # Main chat component
│   ├── message-list.tsx   # Message display
│   ├── code-block.tsx     # Code display with copy/download
│   ├── code-export-panel.tsx # Bulk code export
│   └── ui/                # shadcn/ui components
├── lib/
│   └── auth-context.tsx   # Authentication context
├── types/
│   └── index.ts           # TypeScript types
└── public/                # Static assets
\`\`\`

## API Endpoints

### Authentication

- `POST /api/auth/login` - User login
- `POST /api/auth/signup` - User registration

### Chat

- `POST /api/chat` - Send message and get AI response

## Security Features

- Rate limiting on API endpoints
- Input validation on all forms
- Secure session tokens with expiration
- Password validation (minimum 8 characters)
- CORS headers and security headers
- XSS protection
- CSRF protection ready

## Performance Optimizations

- Server-side rendering for initial page load
- Client-side caching with localStorage
- Optimized bundle size with tree-shaking
- Image optimization
- Code splitting

## Future Enhancements

- Database integration (Supabase/Neon) for persistent storage
- OAuth authentication (Google, GitHub)
- Conversation sharing and collaboration
- Advanced code syntax highlighting
- Conversation search and filtering
- User preferences and settings
- API usage analytics

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Support

For issues and questions, please open an issue on GitHub or contact support.

## Acknowledgments

- Built with [Next.js](https://nextjs.org)
- AI powered by [OpenAI](https://openai.com)
- UI components from [shadcn/ui](https://ui.shadcn.com)
- Styling with [Tailwind CSS](https://tailwindcss.com)

# nature-blog
A nature and home-inspired blog template
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function Blog() {
  const posts = [
    { title: "Embracing Nature at Home", excerpt: "How to bring natural elements into your living space.", link: "#" },
    { title: "Sustainable Living Tips", excerpt: "Simple ways to make your lifestyle more eco-friendly.", link: "#" },
    { title: "The Beauty of Minimalism", excerpt: "Why less is more when designing your space.", link: "#" },
  ];

  return (
    <div className="min-h-screen bg-green-50 flex flex-col items-center p-8">
      <motion.h1 className="text-4xl font-bold text-green-800 mb-6" animate={{ opacity: 1 }} initial={{ opacity: 0 }} transition={{ duration: 1 }}>
        Nature-Inspired Blog
      </motion.h1>
      <div className="w-full max-w-3xl space-y-6">
        {posts.map((post, index) => (
          <Card key={index} className="bg-white shadow-lg rounded-2xl overflow-hidden">
            <CardContent className="p-6">
              <h2 className="text-2xl font-semibold text-green-700">{post.title}</h2>
              <p className="text-gray-600 mt-2">{post.excerpt}</p>
              <div className="mt-4">
                <Button className="bg-green-700 text-white" asChild>
                  <a href={post.link}>Read More</a>
                </Button>
              </div>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}

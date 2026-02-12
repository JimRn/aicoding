<template>
  <div class="ai-products">
    <div class="products-header">
      <h2>中国 AI Agent 产品</h2>
      <p class="subtitle">国内主要的 AI 智能代理产品介绍</p>
    </div>

    <div class="products-list">
      <div v-for="product in products" :key="product.name" class="product-item">
        <div class="product-header">
          <h3>{{ product.name }}</h3>
          <span class="product-category">{{ product.category }}</span>
        </div>
        <p class="product-description">{{ product.description }}</p>
        <div class="product-features">
          <span v-for="feature in product.features" :key="feature" class="feature-tag">
            {{ feature }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AIAgentProducts',
  data() {
    return {
      products: [
        {
          name: '百度文心一言',
          category: '对话助手',
          description: '百度推出的大语言模型产品，支持智能对话、内容生成、知识问答等功能。',
          features: ['自然对话', '内容创作', '代码辅助', '知识问答']
        },
        {
          name: '阿里通义千问',
          category: '智能助手',
          description: '阿里云推出的大模型服务，提供AI对话、文档理解、代码生成等能力。',
          features: ['多模态理解', '企业应用', 'API接口', '个性化定制']
        },
        {
          name: '腾讯混元',
          category: 'AI平台',
          description: '腾讯自研的大语言模型，整合在多个腾讯产品中，提供智能助手服务。',
          features: ['生态集成', '实时对话', '内容审核', '行业方案']
        },
        {
          name: '讯飞星火',
          category: '语音助手',
          description: '科大讯飞的认知智能大模型，擅长语音识别和自然语言处理。',
          features: ['语音交互', '多语言支持', '教育场景', '办公助手']
        },
        {
          name: '字节豆包',
          category: '智能助手',
          description: '字节跳动推出的AI助手，集成了对话、写作、翻译等多种能力。',
          features: ['多场景应用', '创意写作', '学习辅导', '生活助手']
        },
        {
          name: '商汤日日新',
          category: '多模态AI',
          description: '商汤科技的大模型平台，支持文本、图像等多模态内容生成。',
          features: ['多模态生成', '视觉理解', '行业解决方案', '开发者平台']
        },
        {
          name: '华为盘古',
          category: '企业AI',
          description: '华为云盘古大模型，面向企业场景提供AI能力和行业解决方案。',
          features: ['企业级应用', '行业定制', '私有化部署', '安全可控']
        },
        {
          name: '360智脑',
          category: '安全助手',
          description: '360集团推出的大模型产品，融合安全能力的智能助手。',
          features: ['安全检测', '智能问答', '内容创作', '办公协同']
        }
      ]
    }
  }
}
</script>

<style scoped>
.ai-products {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.products-header h2 {
  margin: 0;
  font-size: 1.5rem;
  color: #0f172a;
}

.subtitle {
  margin: 0.5rem 0 0;
  color: #64748b;
  font-size: 0.95rem;
}

.products-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
}

.product-item {
  background: white;
  border-radius: 8px;
  padding: 1.25rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  border: 1px solid #e2e8f0;
  transition: all 0.2s ease;
}

.product-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.product-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.75rem;
  gap: 0.5rem;
}

.product-header h3 {
  margin: 0;
  font-size: 1.125rem;
  color: #1e293b;
  flex: 1;
}

.product-category {
  background: linear-gradient(90deg, #4f46e5, #06b6d4);
  color: white;
  padding: 0.25rem 0.75rem;
  border-radius: 999px;
  font-size: 0.75rem;
  font-weight: 600;
  white-space: nowrap;
}

.product-description {
  color: #475569;
  line-height: 1.6;
  margin: 0 0 1rem;
  font-size: 0.9rem;
}

.product-features {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.feature-tag {
  background: #f1f5f9;
  color: #475569;
  padding: 0.25rem 0.65rem;
  border-radius: 4px;
  font-size: 0.8rem;
  border: 1px solid #e2e8f0;
}

@media (max-width: 768px) {
  .products-list {
    grid-template-columns: 1fr;
  }
}
</style>
